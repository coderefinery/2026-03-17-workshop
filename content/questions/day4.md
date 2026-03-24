
# Day 4

- Week 1  **notes** have been moved to the archive at: https://coderefinery.github.io/2026-03-17-workshop/questions/
- **Videos** from the first week have been uploaded to our [YouTube channel](https://www.youtube.com/watch?v=7_vw7HZZwd4&list=PLpLblYHCzJAAn76NX_JrzvScRcj2I9Frq). These are the raw recordings with the breaks included. Subtitles and editing are still missing, those will come in a couple of weeks.

## Icebreaker :icecream: 

### Have you heard the sentence "hmm... works on my computer"? What does this mean in practice? How do you solve this problem?

- Figuring out the difference between their env and mine
- Check if it differs on Microsoft, iOS or Linux and the installed software differences
- Figuring out all the versions of all the tools ...
- able to run the main.py. Create venv based on the requirements.txt file. 
- Version control!
- When I go to see a system, where it does not work, then it usually works. Modest presense ...
- ...

### What are your experiences re-running or adjusting a script or a figure you created few months ago?

- No big problem if there is readme or howto file, or code is well commented
- Usually works...if not maybe my dataframe looks different
- I work with people who manually edit figures... :scream_cat: 
- I usually mess up with the existing virtual environemnt and it does not work later.  
- Few months? Try a decade. Fascitating, but usually there is a way
- a mess +1
- spending hours to understand +1
- ..

### Have you continued working from a previous student's script/code/plot/notebook? What were the biggest challenges?

- Just do it from scratch yourself :smile: but seriously - to understand how does it work
- Figuring out the reason why some lines are in the code if there are not enough comments
- I also re write it from scratch.+1
- If not clear comments, I have to re-write on my own, in order to follow the footsteps and be able to understand why/how!
- At least it has been easier than from "I copied this from ChatGPT"
- Package dependencies, code style
- The "previous student" had been me, and oh boy how "clever" back then. No psychic could follow those elevated ideas
- I know that some students have continued working with my code, and I wouldn't want to be in their position.. :D
- ..


## [Reproducible Research](
)
### [Intro](https://coderefinery.github.io/reproducible-research/intro/)
### [Motivation](https://coderefinery.github.io/reproducible-research/motivation/)

Your questions here: 

- is this a question? 
    - yes and this is an answer
        - are you sure about this? :smile:
            - no :smile:
- .
- .
- 

## Discussion

::: info
For classrooms: You can discuss among yourself for 10 min; come back to stream approximately xx:28, 
For everyone else: please add your answer below :)
:::

- What are your experiences re-running or adjusting a script or a figure you
  created few months ago?
  - After discovering Pixi as a package manager, pixi.toml and pixi.lock lockfiles things have gotten much easier than with .yml and requirements.txt. I have even managed to have GPU accelerated  workflows across Linux, Windows and MacOS
      - similar with uv / pipenv for me
          - +100 (and pixi uses uv for Python dependencies!)
          - i use uv but not pixi, is it recommended?
              - if you rely just on python packages uv is great (PyPi package index), if you want access to conda-forge and stuff that is not pure Python like CUDA libraries pixi is great (as said above pixi uses uv under the hood)
              
  - Very often some data were missing
  - Very often some instructions, code, and packages were missing
  - No big problem if there is readme or howto file, or code is well commented
  - Usually works...if not maybe my dataframe looks different
  - I work with people who manually edit figures... :scream_cat: 
      - Ohhh, be very careful, it can lead to very nasty outcome: https://retractionwatch.com/2022/12/22/that-paper-with-the-t-error-bars-was-just-retracted/
  - I usually mess up with the existing virtual environemnt and it does not work later.  
  - Few months? Try a decade. Fascitating, but usually there is a way
  - I noticed the problem, tried to solve it commenting, but How to effectively commment my code? I think I going to remember my notes but ..... nop.
  - a mess +1+1
  - spending hours to understand +1d+1
  - In R always using R markdown and knitting them in the end printing out versions of libraries, R, env etc...
  - I usually have problems understanding what I was thinking and how the scripts are expected to work, usually because missing documentation and comments in code
  - I often (used to) struggle with the directory structure, where scripts/data are
  - Usually works fine with minor issues like changed directory and things like that. However, going back to old codes, I always find way better ways to do things more efficiently and in fewer lines :D 
  - Not sure if I dare to update R and packages or if code I wrote earlier will break +2
  - When a new version of a library is realeased I might want to switch to it, but I hesitate because I'm not sure if I can get back to a working setup if I touch anything.
  - sometimes I try to rerun the code from a published paper either to understand it or use for my own research; very often the code breaks.
  - ..
  - ..


- Have you continued working from a previous student's
  script/code/plot/notebook? What were the biggest challenges?
  - Just do it from scratch yourself :smile: but seriously - to understand how does it work +1
  - Figuring out the reason why some lines are in the code if there are not enough comments +1
  - I also re write it from scratch.+1
  - If not clear comments, I have to re-write on my own, in order to follow the footsteps and be able to understand why/how!
  - At least it has been easier than from "I copied this from ChatGPT"
  - Package dependencies, code style
  - Models that were trained with specific versions of algorithms could not run in the newer version
  - The "previous student" had been me, and oh boy how "clever" back then. No psychic could follow those elevated ideas +1
  - I know that some students have continued working with my code, and I wouldn’t want to be in their position… :D
  - I had to maintain a thesis script. The code quality was not high but the actual thesis gave valuable insights into how it was expected to work.
  - Just running old code I wrote on the same machine. Doesn't work anymore and cannot figure out why.
  - Not being maintained any more
  - ..
  - ..


- I have a question regarding what we had to install for today; I could not manage to install Miniforge (it kept on saying that the file was corrupted and contained a virus, so it stopped the installation); so from then on, I don't know how to get the "coderefinery" environment
    - sorry to hear that. And yes it is crazy how difficult it is to get python installed sometimes. :) I assume you have a computer managed by an organisation? (e.g. university computer)
    - Are you doing that on Windows? 
        - Yes, I am on Windows, on a computer managed by my university. I have Anaconda Navigator installed
          - If you have downlowaded the installer from github, you are sure it is without viruses, so you could use a workaround. 
              - I downloaded it from the link provided in the notes for today, so I'm not sure what you mean
          - Anaconda can do that. Start from the anaconda prompt https://www.anaconda.com/docs/getting-started/working-with-conda/environments the rest will be basically the same
                  - Ok i'll try that, thanks
            Anaconda can do everything miniforge does, the problem might be that your institition might have problems with anaconda from a legal point of view (perhaps this is not a problem anymore? Asking someone else to clarify)
                  - Yes the "problems" with the main anaconda channels are still there. but one can use `conda install conda-forge::<package>` to achieve what miniforge does. 

- Stupid question, but I'll ask it anyways: when working in the anaconda prompt to then create the coderefinery environment, I guess I can't just copy-paste the environmnet file that is provided, I have to change the phrasing (since it has to start with the conda create? Sorry, total beginner with environments here)
  - you can download the file somewhere on your disk, and then use the command (IIRC)
    ```
     conda env create -n coderefinery -f <path-to-the-file>
    ```
     where `<path-to-the-file>` is probably just the name of the file, if you open the anaconda prompt in the folder where you downloaded the file
     - this should also work:
     ```
     conda env create -n coderefinery -f https://raw.githubusercontent.com/coderefinery/software/main/environment.yml
     ```
         - Thanks! it works now  :))
## [Organizing your projects](https://coderefinery.github.io/reproducible-research/organizing-projects/)            

Questions continue here: 

- question
    - answer
- What tool can render this folder structure, i.e. `|--` ...?
    - In our case it is a code box in markdown rendered with Sphinx (a tool we will introduce in the documentation lesson tomorrow)
    - Thank you!
        - You can see the source of the lesson on Github here: https://github.com/coderefinery/reproducible-research/blob/main/content/organizing-projects.md
    - If you mean creating a template similar to that structure, then [cookie-cutter](https://github.com/cookiecutter/cookiecutter) is a popular tool. 
        - I mean to automatically show all the files and subfolders in this tree-like view.
            - Perhaps you refer to the shell command `tree`?
                - Oh, maybe. Thank you!

- It happens a lot that the data is somewhat confidential or cannot be publicly available! Was wondering what's the best way aorund? like explain the data and reference from the main provider?
    - Sometimes the best way is to generate and publish synthetic data, based on the confidential data (of course there are caveats to this, like Thomas explained :) ). Otherwise, you can create data schema, and publish it along with your code.
    - With good planning, even the most sensitive data can be shared (e.g. genomic). The problem is that many researchers realize this the day before submitting the paper to the journal. :)
    - The cost of sharing sensitive data though is not low though...

- Not a question, but I'm often using a ready-made template for my projects (https://github.com/NBISweden/project_template), it's been very useful so far (but more suitable for data analysis than tool development)
    - Nice! (+1)

> Moving tags is **evil** but can be done and might be done if a release has some serious bugs/vulnerabilities

- What would be a good way to work when one uses Rmd documents? I am not too sure on how well git is able to keep track of everything in the document. Is it common to also just add version control to the folder and keep using the same document?
  - Rmd documents are plain text files, so git is very well geared to keep these under version control. (But I am not sure I am answering your question)
      - Yes, I think that answers it, thanks :)
        - You might have to be careful about whichfiles you keep under version control (.Rmd files are ok, but any file that is generated from it should not be added)
            - How about RData files? what is a good way to keep snapshots of results. Lets say I have been using git to keep track of my Rmd, and want to keep track as well of the results. What would be a good way to do this? I sometimes save results and add dates, but I feel like there should be a better way.
              - In principle, I would recommend that you keep initial data and scripts under version control (and environments, dependencies...). This should be enough to reproduce your results. Whatever is in your environment as temporary results might be useulf to you to keep for exploratory analyses, but should not be needed to reproduce your research (and nobody else should have to rely on it) [Note: my R tooling knowledge is quite fuzzy, so I might be wrong here]
                  - Great, thank you!! I think that makes sense.
                    - Ther eare also other ways to store your initial data, which might more appropriate that plain version control (but that's the simplest thing - better to find alternatives for "large" datasets)
                        - a "workaround" could be to use hashes -- no backup, but at least should ensure you work with the same data

> Earlier, instructors talked about tags, a topic from last weeks git intro: Read up on it in our git-intro lesson: https://coderefinery.github.io/git-intro/branches/#tags

# Reproducible Publications
`
:::info
Discussion time until xx:45
Classrooms can discuss among themselves
Everyone else add your thoughts below
:::

- How do you collaborate on writing academic papers?
  - They  send me comments and I HAVE to include them.
  - overleaf +2
  - Supervisors send comments in track changes. 
  - Track changes in Word, if others agree to use it. Some don't want to use anything...
  - Overleaf, if other collaborators are open to LaTeX -- otherwise Word with track changes (meh) +1
  - Word document on Teams with track changes and document history activated +1
  - I recommend Typst over overleaf. But there is no collaboration mode yet, AFAIK
  - We use latex on VScode and github, so that it is easy to put the updated figures/plots. 
  - I never do it on a collab env! It is such a mess! They put commetns on overleaf and I address them or eventually explain by putting comments. I find it clearer and more convenient.
  - A bit out of topic: how do you manage references in Word?
  - Google docs. Everyone writes, comments and makes suggestions when they have time (philosophy).
  - ..
 
- How do you handle collaborative issues e.g. conflicting changes?
  - I usually see the history on who changed what. 
  - Adding a comment and the first author often decides. +2
  - I tried using git with LaTeX. The way I avoid solving conflicts just by creating a different branch and frequently checkout.
  - Discuss them over and resolve when everyone agrees (philosophy has to work like this)
  - ...
  - .. 
  - (share your experience)

:::info

## Break until xx:00 (12:00 EET, 11:00 CET)

:::

## [Recording computational steps](https://coderefinery.github.io/reproducible-research/workflow-management/)
Exercises will be shown as demos, you can follow along if you'd like to. You need to have snakemake installed, eg using miniconda:

[Conda installation instructions](https://coderefinery.github.io/installation/conda/)
If you have trouble with the installation, you can join our virtual help room (link in e-mail).
The demo may be a bit fast to follow along, if you are working with these tools for the first time,  so you can also lean back and enjoy and try it out yourself later following the instructions in the material. 

## Workflow-1: Workflow solution using Snakemake
> Instructors are showing the exercise using VSCode, but it can also be run in the command line.

Questions continued: 

- Is it possible to convert Makefile to Snakemake file?
  - hm. Perhaps with AI, but veryfying carefully the result? I don't know if there is a proper tool to do that
      - Thank you!
        - AI tends to be OK at doing these kind of mundane tasks
- I'm using macOS and uv to manage local python virtual environments with specific packages/package versions. Does snakemake work with that?
  - yes, snakemake might work with that. We suggested using conda/miniforge because it can also manage non-python packages, but if you want to configure your own environment it is fine to use uv / fyn / pip / venv
  - 
-^^follow-up question: can I just install both conda and uv then?
  - Yes, you might have to remember what you are using in a particular case, and activate/deactivate environments accordingly. Typically, you will have many "environmets" that can all be used independently. That's the spirit of this "virtual environment" tools: a single user on a single computer can have many of these, which contain only the necessary dependencies for many specific projects.
        -Yep that's how I have been using it. Thank you for the explanation, so UV = just python; conda = also non-python packages
        
- What is the difference between job and core?
    - A core is a physical or logical CPU unit while a job is a process (a piece of work) the CPU is suposed to do
    - a job can have one or more threads, and threads run on a single core, so if a job has N threads it could run on up to N cores (threads can also share a core)
- Our classroom uses R and Rstudio and we are really confused about this workflow. We have tried both cloning the repository to Rstudio and using the binder version.
  - snakemake is a python tool, but it can be used with R scripts too.
  - if you want to remain in R ecosystem, you can use a library called `targets` or `drake` which is make-like worflow tool  
        - I have used targets (a little bit) before, and I was wondering if this was a python equivalent so that's nice to know :)
            - perhaps one should say that targets is a snakemake equivalent :) ehehe
- bash: dot: command not found on Binder
  - this might need to be installed there. Assuming your environment is based on ubuntu, perhaps `apt install graphviz` might work to install it momentarily, but probably you will need to change the environment for this to work in the future. See the following discussion about conda and containers 
  - dot is probably in package 'graphviz' <- yes, corrected comment above
      - graphviz has multiple graph plotting tool for different styles. RHEL-family distros have RPM-format packages and there name is graphviz, but occasionally Debian (apt) uses bit diifferent names. Nice that package name is same in this case
      - fun fact: you can install also from conda-forge. I typically run `conda install conda-forge::pygraphviz` which installs graphviz and the python binding.
          - This worked perfectly on Binder, thank you!
      - Spack:
      ```bash
      $ spack list graphviz
      graphviz  perl-graphviz  py-graphviz  py-pygraphviz  r-rgraphviz
      ```
- ..
- Does snakemake scale well to big modules?
    - I would say yes. But it all probably depends on how you structure your workflow. You can split big pipelines into smaller pieces; there are paramters like `include` (resuse other snakefile) and `module` (resuse another worflow)

## [Recording dependencies](https://coderefinery.github.io/reproducible-research/dependencies/)

Questions continued here: 

- the xz file? watched in Veritasium. https://youtu.be/aoag03mSuXQ?si=m8a7lcwAyyrQmaFt
    - https://en.wikipedia.org/wiki/XZ_Utils_backdoor


### [Discussion](https://coderefinery.github.io/reproducible-research/dependencies/#exercise-demo)

add an `o` for your pick: 

- A : oo
- B :
- C : 
- D : ooooooooooooooooo
- E : ooooooooooo

Questions continued:

- If the reproducibility of our results depends on specific versions, and if when we change the version of the dependencies we get different results, can we really be confident about our results?
    - I think it's hard to give a generic answer, depends on the changes in the dependencies and what the experiment was. Things that can happen:
        - the experiment was a bit overfitted and slight changes invalidate the results (this is what you are referring to I think)
        - the change in the dependency actually introduced a bug (things can slip through :) ) hence this does not invalidate the results
        - If results are about performance, then it's a bit of a grayer area, performance is often a trade-off and speeding up something can slow down something else. It can happen that the developers of the depedency deemed the change worth as it improved performance in several other applications. Some popular packages developers also collect use cases and benchmark changes against those to ensure user don't hit performances hit
- So one yaml with build versions and one with just a list of names is preferred?
    - Roughly yes, this is a typical library vs application distinction. The simple yaml is desirable if you want to always use the latest possible library, as upgrades can be simple bug fixes that you want to get automatically. Note that in the simple yaml file you can still specify constraints if e.g. you know your library needs at least v3 of a dependency. The more detailed yaml file strictly records resolved versions of all dependencies adn dependencies' dependencies and so on

## [Recording environments](https://coderefinery.github.io/reproducible-research/environments/)

Questions continued:

- When to use docker vs docker compose? Is it okay to have different versions of docker-compose files?
   - docker with a single container, docker compose when you need to have multiple containers with different software in them working together. Notice having to use multiple containers, which might have different depdendencies inside, makes things much more complicated. When possible, I'd recommend using a single container.
   - using different containers with docker compose is typically useful when one wants to quickly set up a system with many different parts that are going to communicate via network (e.g., various servers, databases, ....) reusing images that have been created by someone else. This might not be exactly the use case one would like to have in a "reproducible research" context.
- Does it make sense to build container inside a container, e.g., to test different environments?
  - Why can't you just use containers on the host machine? container-in-container setups might be necessary only when trying to automate the container management as well, but that can be usually done with scripting or docker compose
      - Ok, it is probably more complicated to use container-in-container. I got it. Thank you!
- So, basically a container is an image of your system and environment for others to be able to reproduce what you did?
    - roughly yes, you can think a docker image as a snapshot of your whole computer
        - I would not say "whole computer". You select what is the base in container and it does not have to be your whole system. For example, I can create an Ubuntu-based container on RHEL-based system. The environment in container is probably "cleaner" than your whole machine too
          - very good point! I was a bit sloppy in my wording
   - container vs image: image is the snapshot that contains all the files. A container is a "running system" based on an image. Often the two terms are confused, and in some cases they are equivalent (i.e., in the case of immutable containers like in the default case of Singularity/Apptainer)
- I have access to multiple HPCs but I keep on hearing that local machines can be used in many cases as well. In case of container usage, what makes more sense? Use of a local machine or an HPC?
  - use HPC when it takes too long on your local machine (like, more than 10 minutes in my opinion - but for sure if you need to keep your machine turned on while you do other things because your computation take too much time)
  - typically HPC systems nowadays support containers in some way, although it won't be Docker because Docker requires the user to have privileges to run. BUT there are equivalente technologies that can use docker images and run containers.
- GUI applications in container can get tricky
  - you can have web applications that you can connect to via a browser (see the Rstudio docker images, for example)

## Longer break now (1 hour)
Back at xx:00 (14:00 EET, 13:00 CET)

Take a break, have some lunch, snack, coffee, tea; walk around a bit.
We will be back at the top of the hour with a lesson on Social coding and software licensing. 
:::

Questions continued for the morning session :

- Which of there tools are the ones for the bare minimum of good practice? Learning all of them takes a lot of recources, and my workload is already heavy, so it's not possible for me to take on every extensive system right now. 
  - This is true for *a lot* of things, there's always another tool to learn, it's never the end. A reasonable approach is to learn first the things that give you the most value with the least effort. Containers might be hard to learn, using virtual environment tools like venv, or conda takes less time to learn and already gives you more control
  - Thanks for your answer <3
- Well, following the demo on Snakemake, I noticed that the env called coderefinery does not work on that demo! I needed to create a new one just from the .yml in the word-count repo! And then it was resolved! Not entirely sure why though. Could be the different versions of Snakemake in the two envs? Specifically, there is this: "from tenacity import after_log, retry, stop_after_attempt, wait_exponential" then says: "ModuleNotFoundError: No module named 'tenacity' ". And oh, worth saying that I was trying on my own pc and not on Binder! 
    - Thank you for the report. We will investigate!

## Feedback on Reproducible research lesson (in case you will not join the afternoon session)
(add your `o` for the )This session was: 

too fast: 
too slow:
right speed:
too slow sometimes, too fast other times:
too advanced:
too basic:
right level:
I will use what I learned today:
I would recommend today to others:
I would not recommend today to others:


---

## [Social coding](https://coderefinery.github.io/social-coding/)

:::info
Classrooms you can discuss for 10 min (you may want to mute the stream), be back on stream xx:15
Everyone else, please answer below
:::

## Question 1: Why would I want to share my scripts/code/data?

**Choose many**. Vote by adding an `o` character:

- A: Easier to find and reproduce (scientific reproducibility)
  - votes:oooooooooooooo

- B: More trustworthy: others can verify correctness and find and report bugs
  - votes:oooooooooooooo

- C: Enables others to build on top of your code
     (derivative work, provided the license allows it)
  - votes:ooooooooooooooooo

- D: Others can submit features/improvements
  - votes:ooooooooooo

- E: Others can help fixing bugs
  - votes:ooooooooooo

- F: Many tools and apps are free for open source, so no financial cost for this
     (GitHub, GitLab, Appveyor, Read the Docs)
  - votes:ooooooo

- G: Good for your CV: you can show what you have built
  - votes:oooooooooooooo

- H: Discourages competitors. If others can't build on your work,
     they will make competing work
  - votes:o
  
- I: When publicly shared, usually we time-stamp or set a version,
     so it is easier to refer to a specific version
  - votes:oooooooo

- J: You can reuse your own code later after change of job or affiliation
  - votes:oooooooooo

- K: It encourages me to code properly from the start
  - votes:oooooooooooooohttps://diffusion.csail.mit.edu/2026/index.html


## Question 2: The most concerning thing for me, If I share my software now

**Choose one**. Vote by adding an `o` character:

- A: It will be scooped (stolen) by someone else
  - votes:ooooo

- B: It will expose my "ugly code"
  - votes:ooooooooooooo
  

- C: Others may find bugs and mistakes. What if the algorithm is wrong?
  - votes:oooooo

- D: I will get too many questions, I do not have time for that
  - votes:o

- E: Losing control over the direction of the project
  - votes:o

- F: Low quality copies will appear
  - votes:o

- G: I won't be able to sell this later. Someone else will make money from it
  - votes:

- H: It is too early, I am just prototyping, I will write version to distribute later
  - votes:oooooooooooo

- I: Worried about licensing and legal matters, as they are very complicated
  - votes: oooooooooooo


## Question 3: Why is software often treated differently from papers?

Free-form answers:
- "Reward system" is WAY behind the times :+2: 
- Its not peer-reviewed (maybe it should be?)+1
- The code is not formatted for the journals' requirements
- Lack of awareness of many journals of how important software maintenance, software dependencies, analisis reproducibility, environment reproducibility, etc... are for long time. :+1:
- Code evolves much quicker than papers, which need to be more "stable"+1
- No established standard for what a "scientific" code publication should look like +1
- ...
- ..
- ..
- 


## Question 4: When you find a repository with code/library you would like to reuse, what are the things you look at to decide whether you use it?

Free-form answers:
- Quality/cleanliness/ease of understanding of the code
- Amount and quality of documentation, including reproducible examples to "learn" +3+1
- Amount of people using it +1
- Does it actually work when I try to run it?
- Are there examples of the output, examples of functions/commands - does it look useful for what I need it for?
- The pipeline of th work
- license
- How frequently it gets updated 
- Is there an article that describes it in depth?+1
- Are there any descriptions of how to use it? I can figure it out, but do I want to
- Can I understand what's going on and where to find a lot of the codebase
- Clarity of the explanation, and most importantly, having example cases!
- 

Ask your questions here: 

- On the same note of versioning, did not quite fully figured out on how to version your code/scripts! Like over-writing them does not seem a good idea, but on the other hand ahving multiple versions of the same thing is not also nice! Well, it is my understanding that even if re-write, you can still track the changes!
  - Last week we learned how to use Git to create snapshots of your code with commits, and also use tags to signpost special commits as "reference", so that people can refer to a specific version. 
  - Basically, with Git you do rewrite your code, but you have a time machine to go back in time to previous versions - because you took snapshots of your code 
      - Yeah, so you basically track your commits and tags. 

- Since the topic of vibe coding was brought up, I would like to ask what are the major issues that can arise out of the same? I have heard the vibe codes have security issues? WHy is that so? I personally think vibe coding can sometimes be help while writing some small parts of codes but it impedes human learning.
  - "vibe coding" is a very quick way to create some code that at least partially "works", good for exploration. But it's produced without too much thinking by a system  that works a bit like a "fancy autocomplete" based on patterns it was trained on, drawing analogies between your statement of the problem and similar problems solved by others before. One should always double check - or have way to double check automatically - what an AI produces. ESPECIALLY for research. BUT: **join us tomorrow afternoon**, when all of this will be discussed in detail :-)
  - Great! It would be nice if some comments regarding the securities issue is also made tommorrow. 

- I think it is quite hard to do things properly, as I am mostly self taught, what are the best ways to learn how to become better at producing not ugly and robust code?
  - Meta advice: there is always a lot to learn, it will never end. The message here is: there are some tools and practices that it takes only a couple of hours to learn and they can transform the way you work. Mix your work and learning new tools regularly, devote some time every week learning something new (tools but also practices), prioritizing the things that will give you the biggest advantage while requiring the minimal effort.
  - 
- There are some ways of publishing codes that I am aware of. For instance at DTU we have DTU Data repository where one can publish their code and can recieve a doi as well (if I am not mistaken), but can that be considered equivalent to publishing a paper? Also in my case, I have a few codes that are not neccesarily 'confidential' but has limited usability beyond my own work. Insuch a case, is it still advisable to publish my code (eg. on DTU Data if possible)
    - code in a data repository is not peer reviewed, so it is not equivalent to a journal, BUT a journal cannot typically contain code, so publishing code (and data) should be seen as *complimentary* and *necessary* close to publishing a paper with a scientific result.
    - Code that is not reusable, but has been used to obtain research research results, should anyway be published with a DOI that can be cited in the paper that contains those results.
    **--3 So that would mean that the code should be published before the manuscript is submitted?**

- I asked this last week but today is the right session for that. Many people were interested in the topic as well. My question is: What if we published our source code as the supplementary material of a journal paper first? What is recommended to publish the same repository on GitHub later? What is the best practice for this?
    - that might depend on the policy of the journal. I think that you still retain the rights to publish the software, as you are an author, so you should be able to publish it wherever you want - BUT double check. 
            - The author will sometimes give the copyright to the publisher for the content of the article, so if the code is in a supplement you should check first who actually holds the copyright before republishing the code somewhere else
      - (Digression): In some countries, it could also be that you do not own the rights to your own code, but it is your institution that does - if you publish that as open source, with a proper license, you keep the right to work on it after if you change your institution 
      - Yes but if the institution owns it, it might not like you publishing it.
      - You need indeed to clarify with your institution (company?) that you can use an open source license from the start. I would argue that a public institution might typically allow to use open source licenses (with some exceptions). With private companies 
    - How do you expect to receive feedback, if your code is a supplementary in journal? (Possible, but probably easier if it is in Zenodo, which has link to GitHub)
      - typically in the same way you would receive feedback on your paper, which might not be actually as convenient as issues on github (e.g., plain emails)

## [Comparing sharing papers and sharing code](https://coderefinery.github.io/social-coding/social-coding/#comparing-sharing-papers-and-sharing-code)

## Social Discussion 2

1. Have you experienced an implicit expectation of support? add an `o` to your answer

    - Supporting all requests can lead to overworking and mental health issues: 
    - Not supporting requests can also induce guilt: oo
    - Projects are maintained by 1 or 2 persons: o
    - Most projects cannot retain contributors for a longer time: o
    - If you maintain all projects that you start forever, at some point it may be difficult to start new projects: 
    - Other: 
        - Attention is limited.
        - ..
        - ..

Question continued: 
- Is preregistration practical for all domains?
    - Preregistration goal is to reduce degrees of freedom of researchers in deciding about how to analyse a dataset. Preregistration is ideal for hypothesis testing research (e.g. clinical trials), however it can also be used in exploratory research (see for example https://journals.plos.org/plosbiology/article/file?id=10.1371/journal.pbio.3000690&type=printable). In general it is all about being transparent in your analytical choices BEFORE looking at the data. You can still deviate from the original choices, but at least you are transparent about it.
    - Even better is multiverse analysis, multiple team analyse same data with their fav methods and then a consensus is pulled. This goes beyond reproducibility and we start talking about "robustness".
    
- Anyone here using IntelliJ IDE? Sad to hear that Code with Me is sunsetting. Been using this with my supervisor for pair-programming and collaborative coding.
    - With VSCode is possible to do something probably similar (Live share?).
      There's a few editors out there that try to support this kind of pair- (or mob-) programming working style 

## [Software Licensing](https://coderefinery.github.io/social-coding/software-licensing/)

## Question 5: Which of these are derivative works?

**Choose many**. Everyone, please vote by adding an `o` character:

- A. Download some code from a website and add on to it
  - votes:oooooooooooooooooo

- B. Download some code and use one of the functions in your code
  - votes:oooooooooooo

- C. Changing code you got from somewhere
  - votes:oooooooooooooo

- D. Extending code you got from somewhere
  - votes:oooooooooooooooooo

- E. Completely rewriting code you got from somewhere
  - votes:oooo

- F. Rewriting code to a different programming language
  - votes:oooooooooooooo

- G. Linking to libraries (static or dynamic), plug-ins, and drivers
  - votes:oooo

- H. Clean room design (somebody explains you the code but you have never seen it)
  - votes:

- I. You read a paper, understand algorithm, write own code
  - votes:o

Question continued:

- Are LLM-generated texts derivative works? :+1: 
  - Realistically it's up to courts to decide - that's why it's so hard to answer.
  - AI companias of course don't want it to be derivatives, and some court judgements back that up.
  - Others want it to be considered a derivative work...
  - At least now you can read the news and understand what the main question is.
  - Derivative is a difficult word. We can talk about "plagiarism" (ethics) and "IPR/copyright infringement" (law). LLMs can do both (plagiarize and break IPR/copyright) but the responsibilities is in the final user who decides to publish the output.
      - And even the latter question is contentious. The model itself probably is "fine", but any service (like chatgpt/claude or nay other chatbot) the displays the data could be infringing. 
          - They pass the legal responsibility to the user, until some big player complains, then they set some filters... :) In practice generated work cannot be copyrighted so that is their claim... it is all very murky (https://www.reddit.com/r/Futurology/comments/1if79iv/us_copyright_office_rules_out_copyright_for_ai/)


- Is taking a piece of code, renaming all variables, classes and functions and reordering declaration derivative work? 
    - Probably yes.  The core creativity is still there.
    - my personal take: same function signatures -> plagiarism and or license break. Clean room design (same functionality but different architecture) -> no legal issues (but ethical?)
    - I would argue so, but plagiarism here would be very hard to detect, right?
        - It should not be very hard to "tokenize" the two versions to show that they are "identical"
        - The compiled code, or the AST, might be very similar. 
        - Note that "derivative work" is a formally defined thing in copyright law and not exactly corresponding to plagarism
            - Unfortunately derivative is not defined in EU, but it is defined in US copyright law. The closest we have in EU is "adaptation" which is not the same.

- About __I__ not being derivative work, maybe I confused it, but generally it is advised to reference, even if a figure gave you an idea about creating your own figure for explaining a concept for instance, or a code sparked sth about your way of doing things. Not really the same thing here?
    - I think the difference is that here you are not reusing the **work** of someone else, you are reusing the **idea**. Ideas might be covered by patents, and implementations/documents can be covered by copyright. 
- A static library (in C) is just one or more functions. If use of function is derivative, then would it being a library change anything?
    - Good question... if you read about the GPL library and "library exception" you get some related things.  The GPL wants you to consider that linking to a GPL library makes a derivative work.  It probably depends on how much your program is defined around the use of the library (do your creative choices derive from the library's design?)
        - Yes, the library exception talks about how the using code can/has to be licensed

- Let's say I want to use a library that is available on pip to utilize some functions. At some point I want to modify some of the lines of code to implement a further option. If the pip installing is managed/limit by my organization, is it allowed to include the library's needed code directly into my code provided I give the original author their credits?
    - It depends on the license.  If the license is compatible with yours, then yes, you can.  Formally you should list you and other authors under copyright, since now the joint output is a derivative work of the original authors.
    - And scientifically/academically, yes, you should also make sure you give credit.

- If I find a code on some else's public github and reuse the code for my project, is it still important to cite the code? I was under impression that public github codes can be reused. Since we would modify the code for our research, it would essentially become a 'new code'?
  - Two things: copyright and plagirism.  For both of these, even modifying doesn't change the considerations.
  - Copyright: it's definitely a derivative work and you need to consider licenses.  Being public doesn't change that
  - Plagarism: are you presenting something someone else has made as your own (e.g. for academic credit?), or have built on someone without acknowledging them?
    - I am working on a research project that is completely my idea. I have identified the research gap and everything. One part of the project involves use of neural networks. I found some code that can be reused, after modification, in my work. But the research question is based on application of neural networks and has nothing to do with the actual modelling of those neural networks.
      - I'd argue that you are using NN as tools. We don't have to credit the inventor of a hammer every time we hit a nail with it, right? 
   -- Okay. I understand the difference now. 
       - Not the case here, but in some fields you have to ask permission to use some tools (e.g. specific questionnaires for some psychometric trait) so in that case things get complicated (and heard stories of coauthorship given just because a tool was used)
       - It's like if we had a license attached to a hammer - in that case  we need to abide to the terms of that license when using it. Still, 
   
- Is it correct to say that patents cover "ideas" while copyright covers "things produced based on ideas"?
  - Well, not strictly speaking. Patents cover 'technical' ideas. Art is also full of ideas, but not covered by patents at all
  - If you substitute "ideas" for "(novel technological) inventions" then yes basically.
    - Can theorems be patented? Probably not, right?
      - Correct.
      - Theorems and algorithms could be patented if they are implemented and are part of a specific system, which means that in practice algorithms and theorem as we know from school can never be patented (they are generic). 

- How to implement licenses on your own work? Do i just add the file to the github, or is there some kind of larger process that i need to go through?
  - A "wrong" license is better than no license, so while you hope/wait for some guidance from your university legal experts, just add a permissive license and make it easier for you to reuse it and for others to use it and cite you.
  - You might have to check with your institution which licenses you can use for your work. After you've done that, you can "just" add a license in your repository... IF you have the permissions of ALL the copyright holders (this is why you should agree on a license *very* early in the development, not after already many people have contributed, otherwise it becomes very long to get the approval of everybody)
      - "But Sir, our program links to this and that GPL-licensed library. Our hands are tied ..."
  - Some licenses do have instructions that describe how they have to be added into the code (files)

- Do we need a license for this sharing document? :gasp:
   - Yes!  That's why we say in the intro what the license for contributions will be (at least I think we do, at least we say that it will be shared).
   - This is an insightful questions - so many times people do things like this document, forget to think about licenses in the start, and then it essentially can't be reused/shared/etc.
     - but linking it sould be fine regardless of licenses, right? 
     - Yeah, then you aren't making a copy.  (but of course peolpe who want to control data make different arguments, see https://en.wikipedia.org/wiki/Copyright_aspects_of_hyperlinking_and_framing )

:::info

## Break until xx:10
After the break we continue with the rest of licensing lesson
:::

Questions continued: 

- If I get some GPL code, change it, but never release binaries or a product using it, do I need to still publish the code?
  - You don't.  You are't making new copies and nothing in the GPL requires sharing.  If you do share, then you also need to share the source. 
    - Thanks!
  - And just for clarification: Selling a product that uses it (or access to a prodct that uses it) is likely considered "sharing" in this context.
- If i use a libary and copied the example code from the documentation, basically excatly the same, is that something that needs to cited (speaking about 1 or 2 lines)?
    - Legally, perhaps.  Practically, yeah, probably most of us would just do it and not worry about it, and if anyone asks say that we think it's below the threshold of a deravative work.  Good documentation will say a license for the examples.
        - thanks, yes I simply never worried about it, and it seems so normal, but definitly interesting to think about it
> Also for many of these questions, it depends what is your risk?  If you are Google, you treat everything as strictly as possible since you are a huge target for lawsuits.  If you are a normal person, probably not so much.
- Happy to report that we are not Google :P but it is always helpful to be on the correct side of scitific practices and code of conduct. +1
    - Just be transparent with what you do and do ask your legal/IT/ethics/supervisor if your organisation does not have guidelines.

## [Software citation](https://coderefinery.github.io/social-coding/software-citation/)

Questions continued: 

- Chicken and egg: CITATION.cff contains DOI. DOI you get when you sehd it to Zenodo ...
    - Zenodo lets you get the DOI during the process of publishing, so you can add it to the cff file before you push "publish"; it is a bit clumsy, but it works
    - you can "reserve" a DOI on Zenodo
        - Do these include "the linked GitHub pushes a release"?
          - I do not think you can reserve a DOI in that workflow... you might have to do things manually not through github? Not sure if there is a better way.
        - Zenodo generates a DOI that points to latest version, and DOI for each released version. Would the "latest" be more appropriate in the cff?

## [Sharing data](https://coderefinery.github.io/social-coding/sharing-data/)
> If you know of more national (or general) services, please send us a Pull Request to: https://github.com/coderefinery/social-coding/blob/main/content/sharing-data.md

---

## Feedback for Day 4 of CodeRefinery
:::success
News from day 4, preparation for day 5
We went through everything in the schedule, introduced reproducible research and tools that can help with recording environments, computational steps, and dependencies as well as social coding and software licensing.
Tomorrow we will look at code documentation in the morning (why and how you can document your code from in-code comments to beautiful websites) and Responsible use of generative AI in assisted coding.

If you would like to try out the documentation tool, please follow the [installation instructions for conda](https://coderefinery.github.io/installation/conda/).

:::

### Today was (vote for all that apply):
too fast:o
too slow:o
right speed:ooooo
too slow sometimes, too fast other times: oooo
too advanced:o
too basic:o
right level:oooo
I will use what I learned today:oooooooo
I would recommend today to others:oooooo
I would not recommend today to others:


### One good thing about today:
- Recording packages/environments
- I learned one of my mistakes in my current research pipeline
- it forces me to think about stuff that I like to avoid
- The memes :)
- ..
- ..

### One thing to improve for next time:
- Sometimes, I had difficulties understanding the discussions online maybe because of the microphones moderators use.
- Morning session was too fast, challenged to follow the steps +1
- ..
- ..

### Any other feedback? General questions?
- This may be a silly question, but what exactly is _research software_? I’ve done data analyses and GIS analyses and written code related to them, but I assume that doesn’t really count as software, or does it?
  - Not a trivial question! Probably there are multiple definitions possible.
    One possible definition is:
    > Research Software includes source code files, algorithms, scripts, computational workflows and executables that were created during the research process or for a research purpose. 
    
    from [Defining Research Software: a controversial discussion](https://zenodo.org/records/5504016)
    
  - Software, program, tool, command ... doesn't rose by any other name smell as sweet?
    The answer above has a point. 

- A more fun way to enter this topic could be more guessing games...where you cannot see what everyone else replied. It would make it more interactive. 
- Thank you!
- How is it with the certificates? Should these exercises also be included in the report? Which ones?
    - No exercises to include, just as part of your reflection: see point 3: https://coderefinery.github.io/2026-03-17-workshop/certificates
    - Great, thank you!

