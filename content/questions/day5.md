+++
template = "page-with-toc.html"
title = "Questions and notes from workshop day 5"
+++

---

## Icebreaker :icecream: 

### How would you explain your current job to someone in the year 1700? (if you don't know, write what you do and we'll try to figure out!)

- Other people look at things and tell me about it, and I try to figure out why that happened
- I'm trying to figure out the quantity and quality of materials of buildings without seeing the buildings
- I study how learned men message each other.
- I study how insect eat the forest and try to express that with math.
- I study the differences between core esence of tumours compared to healthy tissue (cancer epigenetics)
- I try to understand how we damage the environment because of things we use/consume.
- I try to assess how the things we use influence our planet
- I try to understand how harmful substances in food occurs even before they occurs using mathematics (forecasting food contaminant occurance).
- I build some models describing how things interact and manifest properties.

### What's the best documented project you've seen?

- [Numpy](https://numpy.org/doc/stable/)
- [Xarray](https://docs.xarray.dev/en/stable/)
- In Python anything in rest-style with type hints
- shockingly I can not think of any software that I find super well documented 
- CodeRefinery tutorials +1
    - <3

## [Documentation lesson material](https://coderefinery.github.io/documentation/)

Your questions here: 
- How do i open this view? When I open the code and use conda I use python, not shell. I managed to install the envrionment but I cannot switch
    - Do you use anaconda?
    - Yes
        - There is the anaconda prompt, you see it from the "navigator". Unfortunately I don't have Anaconda anymore so I cannot check the right name.
            - Can it be Anaconda Powershell?
                -  Yes that should work and "see" the command conda, from that terminal.
                -  Alright, I'll try it! Thanks :) 


### [In-code documentation](https://coderefinery.github.io/documentation/in-code-documentation/)

Questions continued: 

- Docstrings can be implemented only in functions and classes, right? But in a snippet when you wanna put a comment on why/how you're doing that part, still have to stick to the #comments, correct?
    - Correct. Docstrings are only for modules/functions/classes.

## [Writing a good README](https://coderefinery.github.io/documentation/writing-readme-files/)

Questions continued: 
- Was wondering what is the logical instances of using a badge? I mean most likely you don't wanna overuse it. Say I am building my code using many other projects like Xarray or another in dev library or a numerical model that is hosted on Git.
    - In one of my bigger projects, I have badges for test coverage (fraction of code run in unit tests), license, tests passing or failing, and one for lauching documentation notebooks on binder (Binder allows you to run the code without installing anything, useful for testing things)
    - They are a colorful way of displaying information, partly verified by a third party. Mostly for color and checking things at a glance.
    - You don't need to put badges for all your dependencies
- .


## [Sphinx and Markdown](https://coderefinery.github.io/documentation/sphinx/)

> You can type along for this session :)

> [Sphinx documentation](https://www.sphinx-doc.org/en/master/)

Questions continued: 
- How to hanlde the "release" or "version" numbers? what would be "1.0" or "0.1"?
    - This could be a lecture on its own :D For your stuff, use what makes sense to you. I like that some projects use a release based on dates (so if it's version 2026.3 I know it is new because it is now)
    - Good!
    - I use semantic versions, but adding a date is a good idea.
        - Semantic version means: MAJOR.minor.patch. patch number changes every time something changes. minor number changes for bigger things, but they are backward compatible. MAJOR number changes can include changes that break previously working code.
- Im getting: sphinx-build . _build  
        ``` 
        Running Sphinx v9.0.4
        loading translations [en]... done

        Extension error!
        ```
    - fixed :), i needed "pip install myst-parser" - great :)
    - Very good! 
      that is why we recommend using the coderefinery conda environment, 
      with that you do not have to install individual packages
      (but of course you're free to use pip if you want more control)
     - I think I did my terminal looks like this: (coderefinery) name@client75-73 doc-example % 

- Would it be possible to show on the screen how to open it from 0? I have troubles with it (starting from an empty windows screen)
    - You mean to open the terminal?
    - Yes, conda and sphinx and everything
        - Are you mac/windows/linux?
        - Windows
            - Do you use Anaconda or miniforge?
            - Anaconda
                - Open anaconda navigator and from there there is the command line (can be powershell or cmd) that will start a terminal with conda visible so you can conda activate coderefinery and sphnix-build ...
                - Oh, I think I have only anaconda prompt! Not a navigator
                    - Anaconda prompt is good. The navigator is like a graphical panel to start various tools.
                    - Alroght, I have a prompt open and I can activate the env :happy: What next? It's not in a shell
                    - I dont understand how to connect it to bash? It's a bit confusing cause I cannot use the code with $ here 
                        - You can try "conda env list" to see the list of your environments. If that works then it should also show the coderefinery environment if you created it.
                        - I did and I called it "word-count" from yesterday's exercise- 
                        - i have it activated now
                        - ok great! So if you just type sphinx-build (and enter) does it tell you some help message?
                        - 'sphinx-build' is not recognized as an internal or external command,
                           operable program or batch file.
                        - you should have also a 'coderefinery' environment:
                          https://coderefinery.github.io/installation/conda/ 
                        - "conda list" will  tell you the list of packages that you have right now in word-count. If sphinx is missing you can just "pip install sphinx" (otherwise you need to deactivate this env, and install the coderefinery env)
                        - It's donwloading now! Thanks :+1:
- ..

:::info

## Exercise until xx:53 

You can choose whichever of the exercises sounds interesting to you! But start with the setup (if you did not type along during the stream)

[Set up a sphinx documentation](https://coderefinery.github.io/documentation/sphinx/#exercise-setting-up-a-sphinx-project) and try out [some features](https://coderefinery.github.io/documentation/sphinx/#exercise-adding-more-sphinx-content)

You can also try out [Sphinx autodoc](https://coderefinery.github.io/documentation/sphinx/#exercise-sphinx-autodoc) or check out using [Jupyter with Sphinx](https://coderefinery.github.io/documentation/sphinx/#exercise-using-jupyter-with-sphinx)

After that we will do a quick wrapup on stream and then go into a short break.

:::

How is it going with the exercises? Add a 'o' where appropriate for you:
- Done:
- I find them interesting:ooooo
- I have problems:
- Need more time:o
- Any comment:
  - I can not get the build to work, probably missed something in the setup, can we see the consol inputs again, please?
      - You can find all inputs before the exercise boxes on the Sphinx material page: https://coderefinery.github.io/documentation/sphinx/#sphinx-and-markdown
      - If you need help, please join the zoom help room :) 
          - My pattern recognision thought that the inputs are another thing to copy into a text file, but now it works, thank you!
              - Nice!
  - The output is beautiful, especially the math and the syntax highlighting in the code
  - I think I also have some problems with setup, but I managed to do the exercises using Command Line and Git Bash simultaneously.
    - very good feedback, for the next time we will try to spend more time on the setup phase to bring everyone up to speed
  - This worked for me:
    ```{toctree}
    :maxdepth: 3
    :caption: Contents:

    [...]
    apidocs/index
    my-new-page.md
    ```
    But I do not understand what is happening behind the scenes, could you explain a bit?
    - did the explanation on stream resolve your question?


:::success

## Break until xx:05 (11:05 CET)

> After the break we will learn how to move our documentation from local to GitHub pages, so that others may also see it :) 

:::


Questions continued: 

- Does the jupyter_execute directory need to be saved or it is generated in the same way as _build?
    - It's generated so you can add it to your .gitignore (as with _build)

## [Deploying Sphinx on GitHub pages](https://coderefinery.github.io/documentation/gh_workflow/)

- How can we know which `uses:` to use in the yml for Github Actions?
    - You can start from the example. In this case you should not need to add any more uses: sections. Extra dependencies can be added by modifying the `pip` line.
    - Thank you!
- I am a bit lost, did we see how the local doc-example repository is deployed? Was it in the template?
  - We move to a new repository using this template: https://github.com/coderefinery/documentation-example/generate . If you click that link you will get a wizard to start a new repository using the template
  - For simplicity, this part of the lesson happens completely on gihtub, but if you want you can also clone your repository locally (the one you generated from the template), and use sphinx-build to gneerate the pages locally.
      - If I want to deploy the same local doc-example repository on my machine using these steps, should I push this local repo to my GitHub page because Sphinx already created these source files in the previous exercise (HTML, CSS etc.)?
        - This is a bit tricky. You could try to manually make a gh-pages branch and add the generated HTML and then push it and not set up GitHub Actions but only GitHub pages -- but I recommend following the way we do it in the lesson
        - notice that the gh-pages branch is a very "weird" one, as it typically is an "orphan" - it has only a commit without parents. You could generate this branch locally on your machine and force-push to github (I have n't tried this, but it could work)
        - In most cases the locally built Sphinx HTML is only viewed locally, but you could also e.g. upload it to web hosting provided by your university. GitHub Pages on the other hand works best with GitHub Actions.
        - If you want to start from the same repository, another possibility would be to move the `.md` files to the `doc` subdirectory as a first step, and then it should be possible to do e.g. `mkdir -p .github/workflows` and make the `documentation.yml`, commit and push and follow the other steps as shown
- (Catching up today so this is only relevant to day four, but I was looking for the coderefinery conda env and the link given on https://coderefinery.github.io/documentation/ is broken. (To https://coderefinery.github.io/installation/conda-environment/))
    - Indeed! Thank you for highlighting, will fix it right away!
        - This is the correct link: https://coderefinery.github.io/installation/conda/
          - Should be fixed now ! :)
              - Thanks!

:::info

## Exercise until xx:35

Try it out yourself: Follow the [setup instructions](https://coderefinery.github.io/documentation/gh_workflow/#demonstration-deploy-sphinx-documentation-to-github-pages) for deploying your own documentation to GitHub pages.

Then try out adding more stuff to your documentation following the [following exercise on the material page](https://coderefinery.github.io/documentation/gh_workflow/#exercise-sphinx-documentation-on-github-pages)

If you have technical issues, please come to virtual help room (link in e-mail)

:::

Questions continued: 

- Huh! Interesting! So basically when you update or modify something in your .md and commit, it basically re-runs itself without prompt and updates the page!
    - yes, when anything changes on the main branch
        - cool!
- where can i click to see my sphinx repository?
    - In GitHub you mean? 
    - yes, in GitHub
    - You can click on your user image > Repositories to see all your repositories, from there you should be able to find it by name
        - Or did you mean from somewhere else?
- At the bottom of the page it is under copyright saying Copyright workshop participant! How to change that? As in the case if I wanted to start from this template and build sth on my own!
    - You can change all kinds of things, also the copyright notice in your `conf.py`
        - Thnx. So 'conf.py' is the place to look at.

## [Popular tools and solutions](https://coderefinery.github.io/documentation/tools/)

> Sorry for the short unavailability of notes! Should be back to normal now :) 
   - thanks!

## [Motivation and wishlist](https://coderefinery.github.io/documentation/wishlist/#motivation-and-wishlist)

## [Summary](https://coderefinery.github.io/documentation/summary/)

Questions continued: 

- Is it possible to integrate DAG (from yesterday's tool: Snakemake) to our documentation?
  - You can produce the picture of the DAG produced with `snakemake --dag | dot ...` (I don't remember the exact command), 
    which is a simple image, and add it as a figure in one of the files.
    It would be good to make it possible to regenerate it every time the snakefile changes,
    and have the render happen on github actions, 
    but this also require you install snakemake - or make it available somehow - in the github actions part.

:::info

## Longer break until xx:00 (13:00 CET / 14:00 EET)

> You may need to reopen the notes link to get back in after a short crash earlier, sorry for the inconvenience

:::

> After break we will continue with:
## [Responsible Use of Generative AI in Assisted Coding](https://coderefinery.github.io/coding-with-ai/)


### [Introduction to LLMs for Code](https://coderefinery.github.io/coding-with-ai/introduction/)

Question to audience: What is your favorite lannguage model/chatbot?

- Not favorite but the university has a license and they say it is more "trustable", Microsoft Co-pilot
- I use CoPilot because my university has a license but I have heard that Claude is a 'good' option as well. After some of the recent releases, ChatGPT has become a huge cesspool of hallucinations. It is so surprizingly bad and people do not realize how bad it is beause they generate such authorative sounding texts.
- All are bad and nobody needs them +
- I'm using mainly ChatGPT bc my organisation offers the paid version
- I'm using Claude and Claude Code
- Claude when I need a solution, perplexity when I need to understand (at least there are sources there)
- Composer 2 from Cursor (looking into Claude atm)
- ive only tried chatgpt

Add your questions here: 

- I have heard that the safest way to use agentic AI (Claude Code for ex) is by using a separate system with no connection to secure networks. What is your opinion regarding that?
  - Agentic AI is the most powerful but most dangerous option. Claude code (and probably also other harnesses) can be configured to an extent, specifying which commands/tools they are allowed to use. If one wants to use the agent without restrictions, then really one should use these kinds of precautions, because there is no way to be sure the agent will not do something incredibly stupid like removing all the files on the filesystem or sending sensitive information to anyone. But...
  - we will talk about this in the Security episode of this lesson
- Note on the Jellyfish report: Jellyfish is a company selling telemetry on AI usage, they have a *financial* stake in how those numbers are represented. They also don't give information on what companies were included in their survey, but companies listed on their website include Draft Kings (gambling). **Consider the source, remember the motive.** +1
    - Well said! As well as the CEOs of these companies saying that everyone will use their product in few months. It would be weird if they would say the opposite. :) +1

:::info

## Exercise until xx:29

Exercise box below [this header](https://coderefinery.github.io/coding-with-ai/introduction/#common-failure-modes)


Goal: Play around with duck.ai and share your relections below

:::

Anything you would like to share about your experience with the chatbot?

- I spelled python as "puthong" and it understood anyway :D
   - yes it mostly works well in fixing typos and spelling errors during writing :D
- It's interesting to test the different models behind duck.ai and compare the difference
  - only one of the models accurately corrects for bias by dividing by (n-1) instead of n
- I tried Claude, it is one of the few big LLMs I have not tried and I was surprised by the speed, love gemini and perplexity but they are often slow (tried a more complex question and like most models exept for gemini claude failed)
    - duck.ai only seems to offer Claude Haiku, the smallest variant. The larger the model, the slower it is, but the higher the chance it can correctly answer to complex prompts.
- I tried both dock.ai and Microsoft copilot. Copilot directly gave me the simplest code with one value error which is raised when the list is empty. On the other hand, duck.ai gave two conditions for raising value error but the second one was kind of maybe unnecessary. 
- Pretty fast, at least using ChatGPT..
  - just remember to be careful about the correctness of the answers too, providing fast responses is not enough :)
     - yes, you are right. I didnt mention that the answer was correct for what I tried.
       - Nice! might be the case for more complex coding projects, which accuracy of the code's funcitonallity is very important but not easy to verify at first glance. In general, its better to use AI tools which are more reliable even if they are not as fast. 


## [Chat based coding](https://coderefinery.github.io/coding-with-ai/scenario-full-control/)

Questions continued: 

> "Slop" is the new Zeitgeist
- My goal in life is to write a markov babbler and fill the training data with nonsense :)
  - this is actually interesting (obviously). I've read somewhere that if you train an LLM with nonsense, it will definitely overfit, while with real data it would do it far less (meaning, probably, that the LLM is really learning "relationships" beween things and creating a model, which obviously does not exist in nonsense data)
- what do you mean by not sharing "real research data" (except obv. sensitive data about anything related to humans)? why is it concern?
    - Two concerns I can think of. 1. this research data will end up in the training data, which means that they can scrape it and use it before you can wrap up your research (e.g. if you're doing material science and they get the patent first). 2. when research data ends up in the training data, the LLM will then slowly learn to generate bogus data, which untrained individuals can then request it to do. this fake data can then lead to misinformation.
- I do know that the 'knowledge' different models are frozen at their training time. However, some of these models also claim to search the web. To me it seems contradictory.
  - the LLM is likely "frozen in time", but the "harness" around it might allow it to call "tools" that are used to bring in its context window information from an internet search. 
  - Asking a question an "plain" LLM is like asking a question to someone who has no access to documentation or the internet at all, and they are allowed to answer only based on what they remember. If you let them search the internet or use a tool, you get something that feels more like a human (because humans typically do some research before answering questions they are not 100% sure about)
- Regarding prompt engineering: it happens to me sometimes that I know that my problem is so specific that I know that I need to tell something very specific to the LLM in order to get anything useful.  
  So while I am carefully crafting the prompt, trying to be concise but without leaving anything crucial out, I realize that I might just write the solution myself in code...
    - Seems like a win no? 
      - It seems like I've got a very sophisticated rubber duck 
        (https://rubberduckdebugging.com/)   +1:P 
          - same for me :D
              - aha! I need a duck
- I used vibe coding to write a script that would query the API of our local train company to find on what day I get the cheapest ticket for a particular destination ("the rise of personalized software")
    - a great exmaple of using AI assisted programming to solve real world problems :)
- Are there any IDE-coding / vive coding / agent tools that don't require personal data to make an account?  I'm thinking as close to duck.ai as possible.  I've wanted to test but haven't wanted to make an account.
  - Anything locally hosted? There are models that can fit in the memory of a beefy computer
- The policies behind the use of AI on copyright-protected data (e.g., local/cloud models used on scientific papers for some data harvesting) can be a bit complicated. How do you deal with this? Who do you ask? University or publishers?
    - Usually a university or research organization should have a policy on the use of AI. I.e. what tools can be used for which applications. Often they have a contract with a specific provider, for which they then allow the use of more "internal" data. If you are an employee at such an organization your manager should know who to contact if you do not. Not sure how the situation for students is.
    - Sensitive data should almost never be fed into a remote LLM.
    - Systems using RAG (Retrieval Augmented Generation) might help with proper attributions of sources (every time you get an answer you also get the information of which documents were used to generate it). Someone more expert than me on RAG could comment here (https://en.wikipedia.org/wiki/Retrieval-augmented_generation)

:::info

## Exercise until xx:59

[Building a data loader and debugging](https://coderefinery.github.io/coding-with-ai/scenario-full-control/#exercises)

Share your experiences below :) 

You can try both or just one. 
:::

Anything noteworthy to share from the exercise?

- I find it very useful to aks for "what could go wrong", it really brainstormed a lot of possibilities I would not come up with myself (maybe also because I did not have a proper context, some of the "criticalities" that the LLM pointed out might not really apply to the problem I have).
- by default they tend to write "horrible" code. the last version of the json loader function is like 50 lines of code, filled with repetitions... giving it a style guide could help (with an agent you can have your AGENTS.md /CLAUDE.md and give some more information on how the code should look like)

:::info

## Break until xx:10

:::

## [IDE integration](https://coderefinery.github.io/coding-with-ai/scenario-ide-integration)

Questions continued: 

> Most reports I've heard about "auto compaction" of the context is that it is not great. I have used it without terrible results. Probably it is going to improve?
> In the case of agents, I believe that very often the harness is not sending the whole content of a file to the LLM server.

## [Full agentic code development](https://coderefinery.github.io/coding-with-ai/scenario-agentic/)

Are you using agentic code systems/AI agnts? Which ones? Any comments?

- I do not have the money to pay for that amount of tokens hah
  - some universities/institutions offer some resources for free (you can use an open source or free agent and connect it to a service for which you get an API key)
- I used Claude Code, let it search through files for necessary information, so it generated necessary code, commandlines itself.
- I use claude code (want to try other tools, I think depending on a single tool is a serious vulnerability) but more as a "pair programmer" than a "project manager"
- I used also OpenCode a couple of times, seemed to work ok (I'm eager to try again)
- Why is Claude installing the slack-app (not part of the prompt)?
  - It is suggesting to do that (as a tip), not doing it (yet). 

Questions continued: 

- How to cosider co-authorship when using these agentic tools? :+2:
  - should the tool be considered a co-author?
      - I am not sure. They also contribute to the works.
         - in my experience, its ok to acknowledge AI tools used for editing or polishing, but not for the scientific ideas, methods or analyses.+1 (I have personally seen very bad research ideas being generated by genAI, at the end of the day AI cannot think, humans can)
         - - There are official guidelines. In the Vancouver Guidelines for authorship, AI cannot be a co-author. They can be used as tool for specific purposes (like refining the manuscript and so on) but finally a human author must review and validate the results produced. And the human is reponsible for the content generated. Like you would not give authorship to the HPC you used to run your calculations, right? 
              - True! But for example Claude Code sometimes offers to commit the changes it made, and when it does, it puts itself as author (funny - with email as norepy@anthropic.com)  
              - - Authorship rules are bound by very specific codes of scientific conduct. Claude can call itself an author as many times as it likes but it cannot be an author in a journal article (or anywhere else).
                - Thanks for the clarification!
                - Plus scientific authorship is different than git commit authorship
              - Are these the "Vancouver Guidelines for Authorship"? https://www.icmje.org/icmje-recommendations.pdf. Yep
                  - Wikipedia says it was 1936. 
  -- If this is an reference to the Vancouver guidelines, they are quite old. But they are also continously updated. I think a more appropriate term would be the updated Vancouver guidelines (I think the part about AI was added in 2024 or 2025)
  - It is definitely a good idea to be transparent about using AI.+1
      - should it be disclosed even when we use the AI only for brainstorming/learning? So the actual code, commits, etc. is made by a person that used AI in the design phase (choosing tools, approach and so on)
          - ..
- Will you discuss usage of CLAUDE.md / AGENTS.md & PLANS.md?
    - We will not discuss this on stream but you can read a bit about it in the materials.
- you mentioned that in 'a few months time' the LLM can perform the coding on our behalf, but ... we still ned to be able to see through the code, understand the code, right. These skills cannot be 'within the LLM' but by us humans - hopefully
    - That's the marketing... +1 Their argument is, that you won't need the skills in the future anymore, because the AI will be so good it can do anything without you checking it. Just like you do not need to memorize as much anymore because we have invented writing. Of course one might not necessarily buy into that hype.
    - yeah it's been "a few months" for a few years now

## [Security considerations](https://coderefinery.github.io/coding-with-ai/security/)

Questions continued: 
- I guess even if the package exists on PyPI, it could have just been made.  So you need to check it's old (and hope that's enough...).  
    - That it's widely used (i.e. downloaded a lot and referenced in other places) and open source would be a good indicator at least.

> The xkcd comic about sql-injections that was mentioned: https://xkcd.com/327/

- In the teaching materials, there is this sentence under Risk 5:... "Here a reddit post with a user completely erasing their laptop with Claude code (add link)". I guess you have been meaning to add the link here. Just a heads-up
    - Thank you for highlighting. Yes, these materials are brand new, and there are a few to-dos left to fill for us :) 
        - Sure! Thank you very much for preparing such thorough open-source materials! :)

##  [Conclusions and next steps](https://coderefinery.github.io/coding-with-ai/conclusion/)

---

## Feedback for Day 5 of the CodeRefinery workshop
:::success
News for day 5 / preparation for day 6
Today, we covered documentation and responsible use of AI in coding. We hope you got to try out Sphinx and remember it whenever you may need a nice polished documentation website. There are a lot of functionalities to explore! 
Tomorrow, the last day of this CodeRefinery workshop: We will dive into automated testing and modular code development. If you would like to try out t he testing exercises in python, please install pytest via our [conda installation instructions](https://coderefinery.github.io/installation/conda/).
:::

### Today was (vote for all that apply):
too fast: o
too slow:
right speed: ooooooooo
too slow sometimes, too fast other times:
too advanced:
too basic:
right level: oooooo
I will use what I learned today: oooooooo
I would recommend today to others: o ooooooo
I would not recommend today to others: o

### One good thing about today:
- Markdown/Github tricks for READMES, intro to Github pages and actions
- didn't know duck.ai
- Great introduction to this, for me, new topics - looking forward to read the text on CodeRefinery too
- The AI coding was new stuff to me and exactly the kind of introduction I wanted to give a broad overview so I know what to know about IDE/agent integration.  (I can learn the rest from here)
- Diversity of topics
- Loved the CLAUDE.md live demo o
- It's incredibly useful session, especially the part about secure using and possible hazards
- Sphinx for GitHub pages, and also for the README!
- Discussing with duck.ai I learned about my own coding mistakes that I will now resolve

### One thing to improve for next time:
- Today's sessions might have been divided into two days because yesterday was more discussion-oriented and we could have seen some of today's materials yesterday already. Yesterday's discussions were necessary for sure, but today's materials were crucial too and I felt that we couldn't go into much today.
- I think that some more discussions on code comments, docstrings and readthedocs would've been nice.


### Any other feedback? General questions?
- The AI session felt very undercooked and very rushed. For a two hour session the scope was far too broad. Some of the technology discussed (especially agentic AI) is itself undercooked, so I question how useful it'll be in a year.
  - a comment: the security considerations around AI agents will unfortunately be quite important for a *long* time (this is a completely new attack vector)
  - It is indeed undercooked by definition as it is experimental, thanks for the feedback and maybe we can focus it more to some aspects rather than covering all scenarios in future CR.
- Thank you!
- Thank you for a nice day

    
