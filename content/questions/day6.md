+++
template = "page-with-toc.html"
title = "Questions and notes from workshop day 6"
+++

## Icebreaker :ice_cream: 

What programming language(s) are you normally working with (add an o for your answer):

- Python: ooooooooooooooooooo
- R: ooooooooo
- Julia: ooo
- C++: oooo
- Fortran: ooo
- Perl: oooo
- PHP: oo
- SQL: oooo
- APL: o
- Bash (shell): ooooooooooooooooo
- Typescript/javascript: o
- AWK, sed: oo
- Nextflow (based on groovy): o
- C o

What does testing your code mean for you? How do you test?

- Part of debugging
- Pytest
- Manual tests making sure the pipeline offers the same results after adding new functionalities/refactor (so really looking forward to automated testing/Github actions)
- assert test == target
- I write automated tests before I code (if it is not exploratory coding), and of course add more automated tests after I wrote the code if something has slipped (e.g., found a bug I didn't think about before)
- to test if the code/pipeline can read the input as expected and write out the output as expected
- nf-test from nf-core

## [Automated testing](https://coderefinery.github.io/testing/)

Ask your questions here: 
- is this a question?
    - this is a question indeed
- Are we talking about "testing" or "automated testing"?
    - in the motivation we are talking about testing in general
    - but we will cover automated testing later too :)
    

> There will be two exercises during this session, see day 6: https://coderefinery.github.io/2026-03-17-workshop/exercises/
> To do the exercises with the instructors in Python, you will need pytest installed, check our [installation instructions](https://coderefinery.github.io/installation/conda/)
> You can also follow the exercise in R, Julia, C++

## [Motivation](https://coderefinery.github.io/testing/motivation/)

Questions continued: 

- Sometimes it happens that I wrote some script, but then trying to make it reusable requires much more thought than just writing it (on which kind of data can I use it?) and then if I'm not going to reuse it what's the point of adding automated tests?
    - Let's assume this is code shared with a paper and I am the reviewer. If I see there is a test and that the test considered some edge cases, I feel more confident that the paper I am reviewing is solid or at least that the script does not have issues with e.g. input validation. If there is no test, then maybe I would start testing the shared code as part of the peer review... but then more broadly: do reviewers actually review the code? (and do researchers share the code?)
        - that opens a bigger discussion: do reviewers even have the time to review the code? 
            - (spoiler: they dont :)... but I do! :D) +1 :)
              
- follow up from previous question: I run my code on know inputs and check visually that it does not fail and that it gives the expected results. Is this testing?
    - Maybe "quality assurance"? :)
    - "manual testing" perhaps?
        - I would say that is the first step on manual testing, but that proper manual testing requires to write some code (maybe just quickly checking in a console output sizes, types and so on, or seeing what happens when using random synthetic data or extreme/trivial cases). Not sure if you meant this already :)
        - and if you find yourself repeating the same manual tests over and over, it is a good sign that you could make them into automated ones (i.e., making a proper script and so on).
- A random question. In my work I have never encountered reviewers asking for the codes used in the actual study. Is this common in other fields? (of course there would be certain studies where maybe the code is the actual experiment)
    - Asking for the code and a "code availability statement" is now common practice in many journals beyond specific fields. Here nature/springer https://www.nature.com/nature-portfolio/editorial-policies/reporting-standards#availability-of-computer-code
    - Not disclosing the code when a reviewer asks for it can be considered academic misconduct and might lead to rejection of the paper.
      - Does this require the code to be open source? 
        - It is not required. You can share private code if needed during the peer review process only. However, open code makes it easier for the reviewing process to share the code with anonymous reviewers. For double blind review there are tools that anonymise the code: https://anonymous.4open.science/ You can also have public repository but with strict copyright without open source licenses. (but people will not build / reuse / cite it)
          - But without open sourceness of course it is going to be hard for anything else than the reviewer to reproduce the results, right?
              - Code can be included as zip file with supplementary materials during peer review process but yes only the reviewer in that case can test / verify... It goes a bit against the principle of being transparent with the research process. Sometimes there might be a reason to keep some code private (e.g. part of a system that will form a patent that is going to be registered)

- What is the standard directory structure for test units? Create a test or tests folder in root? Or right next to your utils.py called utils_test.py?
    - I typically have a test/ directory at the root of my project, (and subfolders) +1
    - It is also possible to add tests right next to your utils.py as you said, but this perhaps more common in other languages besides python. I've seen for example rust projects add unit tests in the same folder

- This might be a Q for later (Github automated testing). I saw that yesterday Github spuns a barebones Linux machine by default to test stuff and installs things via pip. Most of my code use GPU acceleration for image processing (can we have a pixi.lock to define the libraries we need for the testing?) Maybe in this case local tests are easier? Can be also test things on a win-64 machine on Github?
    - Standard runners cannot be gpus. There can be Windows and even Mac virtual machines to run the test / action: https://docs.github.com/en/actions/how-tos/write-workflows/choose-where-workflows-run/choose-the-runner-for-a-job#standard-github-hosted-runners-for-public-repositories
        - Can you define the test to run in two OS? i.e. I want to make sure it works in linux-64 and win-64
    - GitHub enterprise offers gpu runners. or you set up your own runner on a machine you own
    - one can have a self-hosted runner with gpus (BUT there are security problems with self-hosted runners, they should be used only for private repositories IIRC)
    - It is good practice to split your tests so that you can run the bare minimum on specialized hardware. There are many programming models that allow you to write code that can work both on cpus and on gpus, using these instead of something gpu-specific greatly helps testability
        - Keeping in mind, that tests in general should be smallish actions (i.e. minimal) and not run for a long time. At least when talking about unit testing. Long running tests should maybe nly be run before merging to main and otherwise run the small samples, which catch most issues.
            - having toy examples or synthetic data is great for this :)
            - yeah I was thinking of having a small cropped image to run the test on
        
- If I run tests locally can I sync the "tests passed" flag to Github as if it was an action or this is more of a manual step? I test that things work and then I commit to main as said above
    - I don't know, but - first idea that came to mind - you could have a file "localtestpassed.txt" and the action could check that if that file exists, assume the test was passed... just a hackky way :) maybe someone knows more.
        - That is actually a nice idea :), thanks for the input

## [Testing locally](https://coderefinery.github.io/testing/locally/)

:::info

## Exercise until xx:36

Material: https://coderefinery.github.io/testing/locally/#exercise

Goal: Write a test for a simple function, run it, break it (exercise Local-1)


:::

Questions continued:

- Is there a shortcut answer for selecting the threshold when we use some specific values to insert in our test scripts? Like  1.0e-7 that we wrote in the optional exercise. 
    - This depends a lot on the precision that you need for your data and calculations. In this example, we didn't need a high precision so 1.0e-7 is close enough to 0, but in practice depends on your application.
- We wrote two separate test functions in this example. Is this the best practice usually? Or is it just unit testing?
    - It is in general good practice to separate tests that test distinct properties. Depending on the amount of setup needed for specific tests, there can be an argument to avoid multi-setup and just test multiple things in one test after setup, but you can also use something called fixtures for these kinds of situations, where the fixture essentially contains the setup code and then you agai split the actions. 
        - In what Luca is just describing, the numeric tests all test the same properties of the function, so they go in the same test, but the string concatenation is a different functionality, so different test.

- This might be a bit of naive question, but what sort of codes usually need testing? I mean I have functions that create like input netCDF files for forcings for ocean model. So how the test should be crafted? Like checking necessary variables? Dimensions and so on? In more details, it also downscales from global model first, and then creates a file for higher resolution model.
    - To me, there are two cases where I want tests: 
        - 1. Test driven development, where you essentially write the requirements of the functionalities into the tests, and then code until your tests pass
        - 2. Protect against code degration in a larger project in some form of CI system, where the tests essentially ensure, that my logic doesn't change when I modify some functionality. 
      This being said, the test design is most often done so that it ensures, that I get expected values/states after performing specific actions. Like "The data that I wrote to a db is no actually retrievable from the db", if I have data xyz I will get the value xyz when querying via my access functions. 
    - to add on top of the above, I like to use tests when developing code. As Luca was saying at the beginning, tests are a good way to "break your code" and motivate new functionality or realise interesting cases where your current code doesn't run properly. These can be manual tests that might become later automated tests.
- Comment: "breaking tests" typically means to break the code, not to change the test logic. I am actually scared of even touching the tests after I've written them (if you make a mistake when editing the code, you have the test suite to protect you from that, but if you make a mistake when editing the tests you might catch it because the tests don't pass any more, but apart from that you don't have another way)

:::info

## Break until xx:06

> After the break we will have another exercises. If you would like to try it, please fork and clone this repository https://github.com/lucaferranti/example-ci

:::

## [Automated testing](https://coderefinery.github.io/testing/continuous-integration/)

> Luca currently showing: https://github.com/lucaferranti/example-ci
> Following the steps listed here: https://coderefinery.github.io/testing/continuous-integration/#continuous-integration
> Now you can connect with skills you learned in week one of this workshop :)

Questions continued: 


- A general question. I have noticed when you create a repo at first, you add teh first things with the commit message "initial commit". Was wondering if this is a common practice? Kinda makes sense to pin the first commits.
  1. the message "initial commit" is one of the worst possible commit  messages (conveys no information), but it happens very often that there is almost no real work in that commit - so in that case it makes sense
  2. What do you mean by "pin the first commits"?
    - Well maybe bad choice of words, but I meant pin-pointing your starting point. Maybe after numerous commits might been tricky to find.
      - the first commit in a repository will always be the last shown by "git log". Are there cases where this is not enough to make the "starting point" explicit? 
      - It is true, though, that if the first commit contains previous state + actual work it might not be immediately clear what was the starting point. One could use:
        - "starting from template ..." when generating a repository from a github template/cookiecutter template (if this is possible), before doing any actual work
        - "starting from code obtained from ... on date ..." if you initialize a repo that has already some work in it, typically made by people who do not use git, but you want to start using Git (or they use another versoin control system)
  - I agree "initial commit" conveys no information, but also my initial commit generally has no information either :) I generally use a library template to generate the structure of my repo, so my initial commit is generally just an instantiated repo with no real code :) 
    - One could just add in that commit the information that it was generated from a template, and from which template it was generated (not a strong opinion though)
        - good point! and some templates even do that for you I think :+1:
- where can we find these templates for libraries? For example, for developing a python library.
  - (please elaborate? which template?)
      - Luca mentioned that now there are templates to start creating your own libraries, so I was curious about it. For example if I have some python functions and want to create a proper library/package.
      - could be https://cookiecutter.readthedocs.io/en/stable/, for example
          - thanks a lot!
            - happy to help - thanks for clarifying
        - For julia, I use this one: https://github.com/JuliaBesties/BestieTemplate.jl 
            - nice, thanks!
    - Command line tools for python project management, like [poetry](https://python-poetry.org/docs/basic-usage/), [uv](https://docs.astral.sh/uv/#projects) and [hatch](https://hatch.pypa.io/1.12/intro/), also have commands for initializing new python projects based on templates
- A question about licenses from Day4 because I was catching up: I assume that you do not have to follow the license of every dependency that you use (if you don't put their code directly into your repo); but what if you include packages with renv or docker images? Is there a standard procedure for this?
  - I'd argue that creating an environment definition file or a Dockerfile alone does not require you to abide to the license terms of all the software you mention in the definition (please someone contradict me if I'm wrong)
  - Creating a docker image and publishing it might be slightly different?
  - Your Dockerfile definition file is probably not a derivative work (you can have whatever license), but the built image probably is a derivative work and needs to respect all the licenses (at the same time)
      - Note that this is a good reason to make Dockerfiles.  You can share it mostly freely no matter what's inside, no one has to distribute the actual image to others, everyone builds it themselves.
  - [GPL FAQ](https://www.gnu.org/licenses/gpl-faq.html) expresses when distributing GPL and proprietary together is ok:
    > are not combined in a way that would make them effectively a single program.

    Is Docker image "a single program"? Harder to say "no"
    - some docker images can be used as a single program 

## [Test design](https://coderefinery.github.io/testing/test-design/)


:::info

## Exercise until xx:40

Material (Design-6): https://coderefinery.github.io/testing/test-design/#test-driven-development

In the language of your choice: first write the test for the fizzbuzz function, then write the function. (solutions available for Python, R, Julia, C++, Fortran)
We will show it afterwards using Python. 

:::

Questions continued:

- (Question ref. to Design-4) How does monkeypatch work? Why `def test_set_temp(monkeypatch):` can be called before defining `monkeypath`?
  - "monkeypatch" is a function argument, so it needs to be defined only when the function is *called*, not when the function is *defined*. 
  - in this particular case, though, `monkeypatch` is a *fixture* provided by pytest, which works in a different way than just arguments. Anyway, pytest defines this fixture for us before running the test case/function
      - Thank you!
- In which cases is it better to start with the tests? Is there a rule or recommendations for this kind of test-driven design?
    - this is a great question, I'll add my two cents here and someone else with more testing experience will add a better answer hopefully :) There are cases where I have a clear idea of what I want, but not how to get it. I might even have an idea of the structure of the code (like first, I need to compute this, then that), but again developing the code itself will take time. In those cases, writing tests is straightforward and they give me a clear picture. That is, they help me to lay out the structure and start working on the actual code.
        - I find this especially useful when I don't know how to approach the code (e.g., it is really long code or not sure about the tools or even the science/math needed). I would anyway try to sketch somehow the general ideas and skeleton (expected input, output and functions that I think I will need), so writing tests fits very naturally in this step. Of course, I need to go back and forth between tests and code when the project evolves.
    - the questions is also: can you *easily* write tests for a problem? A lot of scientific code faces the so called "oracle problem", where it is difficult to predict the output without actually running the actual calculation (this is pretty much the case for analysis scripts). 
      But there typically are aspects of your computation for which it is trivial to verify the solution, and for those you can write tests, and if you can write tests first then I would always do it.
- When to use `assert` and when to use `with pytest.raise(...)`?
    - The `assert` evaluates expression and reports if the value of expression is not true
    - `assert` is the common case you typically want to use. But when you know your code `must` fail in some particular case, raising an exception, then you want to use 
      ```python
      with pytest.raises(<expected exception type>):
          <code that should fail with that exception>
      ```
     - you can even do `with pytest.raises(<expected exception type>) as exc:` and then do things like `assert exc.some_field == whatever` if you know that the exception has to throw certain errors. I tend to have this for some web services, where I know that functions (not the calls to the endpoints) throw `HTTPExceptions` and check for the status code thrown. 
     
    - An exception is different from "return value of function". It has to be "catched" 
        - Thank you!


> You can find some Conclusions and recommendations in our [lesson materials](https://coderefinery.github.io/testing/conclusions/)


:::info

## Longer break coming up, back at 13 CET / 14 EET

> Coming up after the break: modular code development, no exercises but interactive type along :)

:::

## [Modular Code Development](https://coderefinery.github.io/modular-type-along/)

Questions continued:

- Is also modular code more testable? Or, on the contrary, does it make sense to split your code to test it?
    - (answered on stream, thank you!) 
        - :)

:::info

## Discussion session until xx:25

Classrooms can discuss the questions below offline, others please answer below :) 

:::

A. What does "modular code development" mean for you?
 - Writng codes that can be split into stand alone sections such that corruption of one section does not affect the entire code base.
 - Separating functions in different independent chunks that can be combined like LEGO 
 - Splitting code in reusable blocks. (But how big should the blocks be?) +1
 - Clear structuring of the code with separate functional units and bigger chunks bringing them together as well. +1
 - Encapsulation and refactoring
 - Clarity of mind: if I can build my code to be modular, it means I have a good understanding of what I want and how I'll get it.

B. What best practices can you recommend to arrive at well structured,
   modular code in your favourite programming language?
 - Start with a directory template src, test, notebooks, utils, env +1
 - Start with sketching out the architecture first. +2
     - and I would add reassessing the structure later too, whenever one feel certain part is getting too big or could have a more general scope
 - Well structured == modular? 
 - where to break code? -> when you need "differences": common code parts can become one thing, but things that are different  need to stay separate. e.g., remove as much duplication as possible will in principle automatically bring to modular code (although, one needs to plan for changes that are *not yet* in the code probably, with some planning?)

C. What do you know now about programming that you wish somebody told you earlier?
 - Functions are not just fancy stuff, they are essential to properly structure your code
 - Manage your environments using Pixi
 - Try to generate simple functions, not long ass ones +1
 - Be as organized as possible. Be deliberate, plan in advance and use version control. +1
 - Having test-suite for easier maintenance
 - use version control even for my personal code, this helps to be more intentional in general but I've noticed that aligns nicely with modularity +1

D. Do you design a new code project on paper before coding? Discuss pros
   and cons.
 - It does help me before starting to implement stuff, how it connects, how can I reuse stuff
 - Yes. It helps me to flesh out my thoughts before jumping into the actual coding. It does slow me down a bit. However, I must admit I am not as good at coding as some of my friends hence such a prectice helps me.
 - I don't, but when it's code that needs a design then I usually make a test script that prototypes the functionality, and then for the actual code I can start there and iterate on it.
 - Yes, when it is very complicated, I am always happy when I did and I should do it more often
 - I sketch ideas, but when I want to get started I like to write comments in an empty file to lay out the skeleton of the code. After that, I just need to start adding functions, etc. between each comment.

E. Do you build your code top-down (starting from the big picture) or bottom-up
   (starting from components)? Discuss pros and cons.
 - I want to start from the top, but it can be hard. How can you build the roof of a house without the walls?
 - LLM could be good at giving the big picture, then humans give feedback on what to be included later.
 - I plan out what functions I think I'll need and which functions depend on which, so starting planning from the top, and then I start implementing from the bottom. +1
 - I tend to be quote chaotic and top-down, also pretty results focused and sometimes unwilling to think too much about how to get there

F. Would you prefer your code to be 2x slower if it was easier to read and understand?
   - I would argue that there must be a way to not sacrifice the performance over readibility.
   - I maintain legacy code and some parts are highly optimized sometimes difficult to migrate to new platforms so I prefer easier to understand.
   - Correct is important. Understandable is easier to see to be correct
   - I would prefer it that way, unless performance was critical. Still, I think it is good in any case to have a first version that is slower but clearer to test basic functionality and from there move to optimization and so on.
   -  It depends, if it takes 2s to run instead of 1s but is easier to read then yes, if it takes 2h instead of 1h then no, maybe add some comments and documentation to make it easier to understand +5
       -  In a similar vain: this is also how I approach memory optimisation. +1
   - Can't we just write two versions and automatically test that they are equivalent? so we use the slow version as an "oracle" for the other. 

Your questions continued: 

- How do you define "responsibility"? I've heard a possible definition  - "a reason to change". Do you like this definition?
    - ..
- I have personal experience with badly designed architecture that I have inherited from other collegues. I wish people would think about what they are doing before inserting random patches. I am now left with a legacy code in a legacy language that cannot be migrated to another system. I am wasting my time reinventing the wheel essentially.
    - I feel you, I have been in a similar situation. At some point, I just wondered if it would be better/faster starting from scratch with my own implementation. Sadly, this is not always possible. +1
    - Similarly, the code might be okay but no documentation available, no modularity and so on. That is why it is good that people are starting to learn more about version control and anything covered during Coderefinery, to minimize these problems as much as possible. That won't make anyone's code perfect, but it will ease the experience.
    - Often it is not possible to know how the code will need to develop. And often, it does not develop in the way you predict. 
      Of course sometimes (often?) people make wrong decisions, but it is also due to the fact that some information is not available at the time of taking those decisions. 
      In hindsight, we're always bound to regret some of our decisions, or we will always be able to find reasons why the code that others have written is wrong/badly structured/has some obvious (now) flow.
      If you can "see the future" (or you have experience and can tell how things are going to evolve, typically) you will know where it is best to spend your energies to make your life in the future - and the life of others - easier.
        - definitely! This happens to me even with my own code (wrong or rushed past decisions). It is tricky indeed :)
        - Absolutely agree. It can ceratinly be quite tricky. However, sometimes you see something that is just bad architecture or vibe coded slop. That is not fun to deal with.
- What wuold you say about security issues? Should we learn about those things before writing codes? +1
    - Different languages require different amount of effort -- that is it is easier to err with some
        - Thank you!
- Is there a place within Coderefinery for asking further questions after the close of today's session? (I'm still catching up on day 5 and 6...) +1
    - You can join our chat: https://coderefinery.zulipchat.com and use the #help channel :) 
        - Thank you!

### Modular Code in action 

> To code along, you can find the instructions in our lesson materials: https://coderefinery.github.io/modular-type-along/starting-point/
> You can also just lean back and watch
> In case you would like to learn more about Jupyter Notebooks, check out our lesson: https://coderefinery.github.io/jupyter/

Questions continued: 

- I'm reading along on the .io, and what exactly is meant with side effects in functions?
    - there are "pure functions" and functions with "side effects" (these are the only two kinds of functions that exist)
    - the pure functions ones just take their inputs, and return an output.
      example:
      ```
      def mean(arr):
          return sum(arr)/len(arr)
      ```
      and they do *just that*. Note that mean is not pure, if sum or len or the / has side-effects
      - yes, good point: "impurity" is "contageous"
      - throwing an exception is also a side-effect (e.g when arr is empty)
    - the non-pure functions, that is the one with side effects, to more than that. They might change some data in the background. Save to disk. print something. throw an exception. Adjust global state, and so forth
      example:
      ```
      all_things_ever_computed = [] # global variable

      def mean_with_side_effects(arr):
          global all_things_ever_computed # not sure this is needed
          print(len(arr)) # this is a side effect - maybe not a very "important" one
          
          res =  sum(arr)/len(arr)
          all_things_ever_computed.append(res) # we modify "global state"
          return res

      ```
- (related to question above) are there any reasons why we would like to avoid side-effects at all? I understand in in the case of global variables, but if my function only prints things related to the input or internal variables for example. Or in the case of Exceptions.
  - Let's say that this distinction is important, but in context. There are many possible kinds of "side effects". If a function has *none*, then it's easier to reason about it. But if the function has some "trivial ones", then it does not necessarily means it is complicated to reason about it.
  - Some languages call functions "functions" or "methods" depending whether they return any value. Methods are all about side-effects
  - Exceptions are a mechanism to pass information about an error to the caller, so not "normal" result
    - I see, thanks a lot for the answers!

- Not a technical question but another type of question :) Could you please share this Jupyter notebook with us? :)
  - Do you mean the final product? Or which part of the notebook? This is kind of "work in progress" at the moment
  - I mean the current form developed just now, just to see how we changed the modularity compared to the original version.

```

import pandas as pd
import matplotlib.pyplot as plt


# read data
data = pd.read_csv("weather_data.csv")

# combine 'date' and 'time' into a single column 'recorded_at' as type datetime
data["recorded_at"] = pd.to_datetime(data["date"] + " " + data["time"])

# set 'recorded_at' as index for convenience
data = data.set_index("recorded_at")

def plotdata(x, y, y_label, location_label, color, *, show_y_mean=False):
    fig, ax = plt.subplots()
    
    # temperature time series
    ax.plot(
        x,
        y,
        label=y_label,
        color=color,
    )

    if show_y_mean:
        values = y.values
        mean_temp = sum(values) / len(values)
        
        # mean temperature (as horizontal dashed line)
        ax.axhline(
            y=mean_temp,
            label=f"mean {y_label}: {mean_temp:.1f}",
            color=color,
            linestyle="--",
        )
    
    ax.set_title(f"{y_label} at {location_label}")
    ax.set_xlabel("date and time")
    ax.set_ylabel(y_label)
    ax.legend()
    ax.grid(True)
    
    # format x-axis for better date display
    fig.autofmt_xdate()

    return fig


MONTHS = ["2024-01", "2024-02"]

for month in MONTHS:
    # keep only january data using datetime period indexing
    january = data.loc[month]

    fig = plotdata(
        january.index,
        january["air_temperature_celsius"],
        "air temperature (C)",
        "Helsinki airport",
        "red",
        show_y_mean=True
    )
    
    fig.savefig(f"{month}-temperature.png")

    fig = plotdata(
        january.index,
        january["precipitation_mm"],
        "precipitation (mm)",
        "Helsinki airport",
        "blue"
    )
        
    fig.savefig(f"{month}-precipitation.png")
```

    - Thank you!
- In which cases would you add a function at the top of a given script as opposed to a new script alltogether?
  - On tendency, I would almost always split into different files (modules), and have similar functionalities grouped into one module.  
    I wouldn't keep it in the same script since I can't reuse it elsewhere then. Only if this is really closely related with the script would I have it in the script itself.
      - So, group funcionalities in, say, a 'preprocessing functions' and a 'postprocessing functions' script?
        - a common structure I can imagine would be:
          ```
            - io 
              - preprocess.py
            - processing
              - structure_analysis.py (containing different algorithms for stucture analysis)
              - prediction.py (prediction things)
            - plotting
              - plot_for_result_type1.py              
            ...             
          ```
        - this is a structure that would match many project. I would argue that one should also try to use structure (and the names of the things at the high level, modules names/file names and so on) to convey meaning, so that if one just looks at the project structure it understands what it does (perhaps obvious? but for example "preprocess" is very generic, typically there's more information one can express.) (Not a strong opinion) 
  - If there are many things to change, you could just go for a new script BUT I think that people take that road way too often.
  - C/C++ executables/libraries are built and linked. If the additional helper function is an implementation detail -- not of use anywhere else and something that should not show on API, then they can "hide" is same file
  - to add a small comment, this depends in which stage you are in your coding project. When you are starting, you might yet not need a big structure and might even have a few functions in the same script with a common goal (e.g., analize data X) but different functionality (preprocess, analysis, plot, ...). But as soon as the code grows, and you start finding subgroups of functions with common functionalities (for example, several pre- or post-processing functions), it is good to move to an structure like the example above (folders for each big general functionality).
    - Sounds good. Thanks


:::info

## Break until xx:00 (15 EET, 14 CET)

:::

Interaction possibility for the audience; what should Frankie do next to get to more modular code? Add your suggestions.

- [x] Write a `plot_multiple_data(months)`
  - we could hve a single month function and "just" use a for loop around it?
      - Then, we could define two separate functions, one for a single month another for the loop
  - Should the multiple monts be overlayed, or simply a date range as one plot? 
- [ ] Writing a function for plotting different data, i.e., temperature, precipitation, etc.
- [ ] make it able to choose a month and amount of months plotted
- [X] can we add keyword arguments to the function calls? Otherwise it's a little hard to understand if we're using the arguments correctly (I know this is a little python-specific)
- [ ] Is there a debugging mode or sthg so we do not have to reload the kernel everytime we implement a change in our utils.py within the module?
  - there is, I think, some "magic" commands for jupyter that make sure that the kernel checks ~~(on ipython there was something like `%load_ext autoreload 2`)~~ - not sure it works now! (will double check) 
    - this should work (just tested):
      ```
      %load_ext autoreload
      %autoreload 2
      ``` 
      but should be at the beginning of the session
      also, the first line might not be necessary - autoreload is actually loaded by default, it seems
  - this could work i guess - import importlib, utils; importlib.reload(utils)
    

Questions continued: 

Question: how can we sure that we don't break something during the modularization?
- Tests :smile: , if you write tests for the individual functions that can work but in this case would actualy be difficult, because e.g. the output files are always different (generation metadata is changed)
  - end-to-end?
      - you could take one or two examples of figures and save the actual matplotlib objects, and then compare properties of the objects. Doesn't need to be end to end (which actually wouldn't work here). but what you could try is comparing the contents of the actual images (pixel contents, not the files), since those should stay the same.

- Is there a good reason to use click instead of argparse? Just wondering, since I didn't know about this option.
    - Description of click starts:
      > Simple wrapper around optparse ...
    - argparse is probably more standard, with click it is easier to do things like sub commands (think how git works, that you have `git pull`, `git commit` and so on - sub commands, but that's also how other "modern" command line interface work - docker/podman/apptainer, conda...) 
    - click has a few nice things about it, but argparse works just as well in most situations.
        - thanks! I will take a look into it :)


## Feedback day 6

### Today was (vote for all that apply):
too fast:o
too slow:
right speed:ooooooooo
too slow sometimes, too fast other times: o
too advanced:
too basic:
right level:ooooo
I will use what I learned today: oooooooo
I would recommend today to others: ooooooo
I would not recommend today to others:
    

### One good thing about today:
- Hands-on practices were perfect! Thank you very much!
- Really liked the test-driven development exercise, it was a fun way to think about things!
  - will probably reuse this in my training events
- Live demo and interactions
- It was interesting hearing from regular users of these tools!
- This course has been what I really needed in my research at the moment, I already started rebuilding my projects based on what I learned here. Thank you!
    - <3
- ..
- ..
- 
- 

### One thing to improve for next time:
- ...
- ...

### Any other feedback? General questions?
- Modularizing code/architecture is a difficult topic
- Thank you!
- Could you provide the modular exercise outputs that was done today? The final version what I mean. Thank you!!
    - Okay, thank you so much for referring to that! I wasn't aware sorry!
    - Just in case it helps: https://filesender.funet.fi/?s=download&token=fa838315-0a60-407b-af9a-7ae32c55f9c6
- Thank you for the great workshop! I learned a lot! :smile_cat: 
- ..
- ..
- .

---
