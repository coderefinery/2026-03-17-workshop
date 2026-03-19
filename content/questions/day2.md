+++
template = "page-with-toc.html"
title = "Questions and notes from workshop day 2"
+++

# Notes - CodeRefinery workshop March 2026 - Day 2

## Icebreaker

### What was the last animal you saw?

- Squirrel eating all the leftover bird food from terrace 
- A crow collecting nesting material in my yard (spring time yayy)
- My sleepy turtle :D
- a cat
- titmouse
- mostly human (+2)
- many small humans
- guinea pig OWO
- a bunny
- My cat - very early this morning at 5.42 AM
- My dog o
- Red fox
- A city-bunny (which is more like a giant bunny)
- a bird
- two crows.
- Several doggies on my way from the office yesterday :D
- My chinchilla
- My cat (who is meowing at my office door!)
- a magpie out of my window
- Homo sapiens
- Great tit (parus major) D
- birds
- A very friendly dog
- A pheasant
- Humans apart, a group of deers in Sweden
- Sleepy commuters on the tube
- Squirrel crossing the road
- My doggie> []> []
- A magpie
- My cat on my desk right now
- Lion
- A bird
- A fox
- A dog and humans o
- 2 adorable kittens
- ..

### Poll: Which path did you use yesterday to interact with Git?

Add an 'o' to the answer that applies to you:

- GitHub: oooooooooooooooooooooooooooooooooooooo
- VSCode: ooooood
- RStudio: 
- Command line: ooooooooo
- I was not here yesterday (no problem): ooooo
- Github
- I wished you offered a path for a different tool (which one?): 
    - ..
    - ..

---

## Any leftover questions about the workshop in general or day 1 materials?

- How do you find software on Github, if not coming directly from a publication?
    - That's a good question. I search with search engines and then find maybe the github repository.
    - There are also some "software directories" that some institutions might have, that can be searched for relevant research software (in Germany we have https://helmholtz.software/, for example)
        - There are also some directories for domain specific tools, like https://bio.tools/
- No questions but yesterday sessions were great, thank you! Looking forward to today and days to come. (+2)
  - Thank you! :heart_eyes_cat:
- having terrible echo in sound
  - are you in a in-person room? or alone? Do you have multiple instances of the twitch stream running, by any chance? Is your microphone on? (just trying to troubleshoot, I have no problems with audio)
  - thanks, had multiple instances running

## [Cloning a Git Repository and working locally](https://coderefinery.github.io/git-intro/local-workflow/)

- Where exactly on Twitch would I find the videos from previous days?
  - On Twitch you can find already the video from yesterday, ~~it might be already on~~soon also on youtube in the CodeRefinery channel
- Where is git history stored locally? Can it take substantial storage for a big project?
  - You can see it in the "network" graph on github - you will see this later too.
- .
- Can you treat and think about GItHub repository as a folder system? For us that use R projects, can you have several repositories within a repository. For example, if you have one large, main project and several subprojects, is it better to make repositories within a main repository or would it be best to have separate repositories for each subproject. What are the drawbacks ?
  - typically having repositories inside another repository is not recommended (there are ways to do this, more or less, if it is really needed).
  - You can look up "git submodules", but that is not "repos within repos", it is more a "content from many repos in one work tree"
  - But I would argue that the best is to have a single repository, with different directories inside. Multiple people can easily contribute to the same repository, this is basically the most interesting feature of Git.
  - In my experience, most people that decide to go for multiple repositories instead of one are then dissatisfied by the complexity of the result.
  - Technically, you have a tree of working files that has however many subdirectories (if needed). At the root of that tree is the `.git` directory that contains the actual "repository". You don't want other repos in subfolders

- Is it possible to speak a bit louder or turn up your mic a bit?
  - Are you unable to increase the volume on your side? 
  - We have increased audio volume as much as possible on our side, but still can barely hear the two instructors
    - There are multiple volume controls you can use: the Twitch interface has one on the bottom left of the window... could that be that that one is low? I can hear the stream fine and I can also make it very loud 
    - Will check again but seemed to only allow muting and we checked all system volume
    - Samantha and Enrico were fine in terms of audio volume here, but the two instructors we almost can't hear
    - Aalto room here and volume is very good. The risk of increasing the source volume is that it will distort.
- Can you turn up the volume of the stream a bit? :)
    - Volume increased a little bit. You will hopefully "feel" it in about 15 minutes.
    - We feel it yes, thank you (DTU room)


## Exercise until xx:35
Exercise link: https://coderefinery.github.io/git-intro/local-workflow/#exercise

Goal: Go through the steps in the exercise
    - clone a repository of your choice, e.g. [recepie-book](https://github.com/cr-workshop-exercises/recipe-book)
    - create a new branch
    - make a commit
    - switch to main
    - merge the two branches


- sorry, didnt got the instructions for the exercise. 
    - Sorry we were a bit slow with adding the links above. Now clear?
    - Instructors will also go through it step by step afterwards in VSCode
- was it "Just do it"?
  - yes :) -> Follow the steps here : https://coderefinery.github.io/git-intro/local-workflow/#exercise

- I'm using both VSCode and Rstudio for my code, would it be best to choose the terminal path to cover them both?
  - You should be able to interact with git from both programs, but there are some quirks. Make sure you always save your files to disk before doing any git operation... but I think yes, using the command line in this case might be most convenient, so that you have a tool-independent way of dealing with git repositories - which is also more powerful. If you wish to learn it!
  - You can also check the steps in command line, VSCode and RStudio (shown as tabs) underneath the exercise box
  - The tabs let you pick your own adventure :heart_eyes_cat: 

- What is the benefit of using switch than checkout?
  - "switch" is a newer command that was created to work on branches, while "checkout" does many things, which look too confusing (checkout can be used to switch branches, but also to operate on single files... )
  - "switch" is more focused on changing branches but "checkout" can also do other stuff like restoring fiels.
  - Thank you!
  - Naming git commands is hard
      - Naming _anything_ is hard

-  when typing: "ssh -T git@github.com"  i am getting "git@github.com: Permission denied (publickey).""
    - You did not set up your ssh keys OR ssh agent is not running. If you need help with this we are in zoom, otherwise the instructions are here: https://coderefinery.github.io/installation/ssh/
    - yes, i need help ;)
        - Were you able to join the support zoom (link in e-mail)?
        - i was trying to do it myself. but now seems not needed (?) 
        - im going there
    - `ssh` is not needed for this part of the exercise; only after lunch
    - what is not needed for this part of the exercise?
    - Sorry this was a bit confusing. So in general the ssh setup is not yet needed in this exercise but if you encountered it already, better to do the setup :) 
    - the instructions indicate "Configuring Git command line and editor" so

- What should I type in the terminal in VSCode to see the graph? Instructions seem to stop after showing how to open a terminal window.
  - First open the terminal in VSCode
  - You can then follow the instructions from the command line tab in the VSCode Terminal. 

- What is written in the terminal (same as above)?
    - `git config --global alias.graph "log --all --graph --decorate --oneline"`  for the graph (see the command line tab under [step 7](https://coderefinery.github.io/git-intro/local-workflow/#how-to-compare-the-graph-locally-and-on-github) )
    - I can see now. FYI It's not in the "VS Code" tab in the step 7 
        - Indeed, it is only mentioned in the text above the screenshot. But we will make it more visible, please add any comments you may have about this to this issue: https://github.com/coderefinery/git-intro/issues/527

- I am getting this when configuring git hub when running the command [ssh -T git@github.com: git@github.com]: Permission denied (publickey). What should I do?
    - Have you added your public ssh key to your GitHub account?
    - I have, for another project's repository. Do I need to use it for all projects from now on?
        - maybe it is your ssh-agent not running? (assuming that this other project repository is in the same computer and it has worked before)

- I would love a detailed explanation of how local branches and remote branches interact with each other. Yesterday I was coming across some interesting behaviour where I locally renamed a branch locally while it was tracking a remote branch, and VSCode didn't automatically adjust the name of the remote branch. So I'd like to understand their link better. 
  - remote and local branches are, in principle, just different references. 
    Git remembers, locally, which local branch is tracking which remote branch. This can actually be configured in a pretty custom way, but typically, when you push a new local branch a remote branch with the same name is created, and when you pull a new remote branch a local branch with the same name is created. If you want to see the mapping, you can have a look in ".git/config" in your repository, there will be some `[branch "branch-name"]`  sections which define to which remote branch each local branch is mapped.
  - what happens locally is never automatically reflected on remote (at least with the tools we use here). So I could rename a branch and never push it back to remote  
      - Right but I did push back to remote, and it created a new branch on the remote instead of renaming the original branch. So locally I had two branches (main, renamed) and on the remote I had main, old name, renamed
        - Yes that is correct. Renaming is kind-of "create a copy and delete the old one", but the "delete the old one" is not happening automatically. 
        - Locally, `git branch -m` is clever enough to "create a copy and delete the old one", but doing this remotely is actually tricky. What if someone is already working on the old branch? Are you going to change the name of the remote branch while they are working on it? What should really happen then? It's complicated...
            - Thank you both for the answers! This clears things up. I like thinking about it as a smart copy and delete, that makes sense.

- What is the difference between fetch and pull?
  - "Fetch" only downloads the latest changes from the remote repository to your local machine repository, so it does not changing your files. but "pull" downloads the changes and automatically merge them into your current branch in your machine.
  - According to `man git-pull` the pull calls fetch and some other operation

> Is the volume better? We have now raised it up to 11. :guitar: 
> - Yes, much better. Thanks! :smile:

- Do we have to use ssh for the coming exersices or does https work fine?
    - After lunch ssh needs to be set up. You can join the help zoom (link in email) if you need support
    - GitHub (and almost any other remote git host service) does not allow weak authentication (https), it wants strong authentication (ssh keys, MFA, etc..). This changed happened a few years ago.
        - If I am using the command line within VS Code, the authentication happens through VS Code, right? Should I still use SSH?
    - With HTTPS you can only read what is public. For write _as you_ you have to authenticate, that is git to use ssh

- When using `git branch --all`, where do "remotes" come from, and why when using `git switch `, we don't need to add "remotes/" in the branch name ("origin/...")?
  - `remotes` are a way for your local git repository to keep track of the state of the remote repository (you update these when you pull) 
  - when you use `git switch`, you never switch to a remote branch. If you do `git switch remote-branch` , actually a new **local** branch called `remote-branch` is created in your repository.
  - Thank you!

- I am trying to git push the new branch i created locally, and then git was crying for upstream. is it the best practise to use `git switch --track origin/<new_branch_name>` locally instead of using only `git switch -c <new_branch_name>`? Alternatively, when i tried to do it yesterday to do `git push` with the same case, i used the solution ` git push -u origin <new branch name`. Which is better?
    - basically you will need something like `git remote add origin git@github.com:USER/myproject.git` and then `git push -u origin BRANCH` and this is what we will do after the lunch break. And its meaning will be covered then. :)
        - I dun quite get what does it mean with the `git remote add`
          - `git remote add` is the way to tel git "hey, there's a remote repository you can do push to/pull from". When you clone, the "remote" repository is automatically set up. But if you haven't cloned, then you need the `git remote add ` command to tell your local git about the existence of the remote repository (e.g., the one on github).
          - with `git remote add origin git@github.com:....` you're telling git on your local computer:
            - there is a remote repository it can access via ssh at git@github:....
            - this remote repository is called "origin" 
        - do i do `git pull` to syn the local branch as well?
          - that should work, if the local branches are configured properly. 
            you might have to use the full command `git pull origin <name-of-the-branch>`.
          - If that does not work, git tends to give you some message which should be relatively helpful (e.g., tell you another command, that you might need to slightly change, to fix things)  

- when committing, I get an error saying that I need to configure user name and email in git. How do I do that?
   - This is happend because Git needs to know who is making these commits, you can set your name and email adress using git commands:
     `git config user.name "Your Name"`
     `git config user.email "youremail@example.com"`
    - Link to our instructions: https://coderefinery.github.io/installation/git-in-terminal/#configuration

- Am i the only one who's completely lost? (+1)
  - You can come to the help room during the next break or exercise break and we will be glad to help (you could come now, but it might still be beneficial to try and follow the instructors)
  - Brief overview going on right now. :)
  - But they are not going through the graphs (which was the confusing part)
        - What was confusing about it? Maybe we can help here?
        - That the terminal doesn't work for me, it doesn't give me any results

- will we cover the difference between merging and rebasing, and when it is appropriate to use these? (+1)
  - Rebase is a little complicated...
  - I would also really like an explanation on merging vs. rebasing. All I know is that rebase is a thing that's recommended on stack exchange sometimes.
  - You mainly use merging when you want to combine branches and keep the full history of all changes, but when you do rebasing, it makes the history linear and rewrites the commits.

- Perhaps it will be covered in a later session, but if I have an Rstudio project with local version control, can I use that to create a new project on github remotely from Rstudio?
- Or would I need to create an empty repository on github and merge everything to it? Would it show all my locally committed commits?
-   - Not an RStudio expert here, but I *think* that you will still need to create the remote repo outside of RStudio and then connect the two. If you do the merge with git, it should keep all your commits. 

- What does a star next to a branch name when running [git branch --all] mean? Does it mean that is the branch I am working in?
  - yes! That's the current branch you're working on (that should be the output of the simple `git branch` command without options or arguments)
  - Indeed. Example:
    ```bash
    $ git log --all --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d %Cgreen(%cr) %Creset' --abbrev-commit -n 14
    * 64e0eab - (HEAD -> interface) (3 weeks ago) 
    * 6be17bd - (tag: v1.3.0, origin/releases/v1.3, origin/main, origin/HEAD, main) (3 months ago) 
    * 74f0b7f - (3 months ago) 
    *   5098115 - (4 months ago) 
    |\  
    | * 5717576 - (5 months ago) 
    * | 8582c2c - (5 months ago) 
    * |   bba8da1 - (5 months ago) 
    |\ \  
    | * | 87da5da - (5 months ago) 
    | |/  
    * | c11c3f3 - (5 months ago) 
    * | c829763 - (5 months ago) 
    * | e2a335c - (5 months ago) 
    |/  
    | * 8d1e45f - (varity) (5 months ago) 
    | * 4edf1f7 - (5 months ago) 
    |/  
    * 191a315 - (7 months ago) 
    $ git branch
    * interface
      main
      releases/v1.2
      varity
    $ git branch -a
    * interface
      main
      releases/v1.2
      varity
      remotes/origin/HEAD -> origin/main
      remotes/origin/main
      remotes/origin/releases/v1.2
      remotes/origin/releases/v1.3
    ```
    - Great thank you!

- Will we discuss how to roll back to a previous point in history?
    - Kind of yes with inspecting history, but the full exercise on that is an optional one https://coderefinery.github.io/git-intro/recovering/

- should I click on "publish branch" to be able to push the changes frm my own branch to remote?
    - On VSCode, this is the way you publish your current branch to the remote rpository (if I recall correctly)
    - Yes, clicking "publish branch" in GiHub creates the branch on the remote and pushes your local commit there. After that you can push future commits using `git push`.


# Break until xx:05
Remember to stretch your legs and drink something.

Questions continued here

- I got these when trying to merge in VSCode terminal: [UW PICO 5.09    File: /Applications/Desktop/CODE/CodeRefinery Workshop/recipe-book/.git/MERGE_MSG    Modified  Merge branch 'another_branch'# Please enter a commit message to explain why this merge is necessary, especially if it merges an updated upstream into a topic branch. Lines starting with '#' will be ignored, and an empty message aborts the commit.] But I am not sure where to write the message and specially how to exit this window after writing the message.
    - This worked for me: https://stackoverflow.com/questions/19085807/please-enter-a-commit-message-to-explain-why-this-merge-is-necessary-especially 
    - thanks!

- The `github.githistory.xyz` site cannot access non-public repos
   - Yes thats correct, it just work on public repositories. 

- The terminal doesn't give me any results. It only shows "PS C:....\networkx>". I am not sure what to do. I was hoping that the last part of the last exercise will be shown (step 7).
    - Is that PowerShell terminal in Windows? (I don't use those)
    - It's the terminal in visual studio "View-termianal"
    - The PS ... well command like `dir` probably list files
    - I figured it out! I see that in the terminal I had a powershell and I had to put the little arrow next to the plus and switch to "bash". Now the rest works :)

- The _search_ in 'less' is forward slash `/`, not backward slash `\`. More generally, the git command starts a "pager" to make browsing the output easier. The default pager seems to be the 'less'

- How do I fix it? In the twitch, they have "coderefinery %" I don't have anything like that. It starts with the "PS C:....\networkx>" on default
    - All that text is just a "prompt" -- nothing to care about. Different terminals use different prompt strings

- When viewing very long messages, how do i go back to the main line where I can run commands? I am stuck at : 
    - fantastic, thanks
    
- Are there fundamental differences between Command line and using the Terminal in VS Code, for example as was mentioned that Command line is more powerful?
    - My assumption is that VScode runs command line git commands in the background. Command line is useful as you can automate things, git add files depending on some pattern (e.g. git add *.png // add all pngs)
    - Everything you can do in the command line, you can also do in VSCode terminal. VSCode is just more convinience as let you run commands in same window.
        - VScode terminal _is a_ terminal. Every terminal has command line. Thus it "is/has" command line

- Could you repeat how you got that long hash code for the particular commit that you rolled back to?
    - The hash does not have to be long. Just long enough to bu unique
    - Try `git log --pretty=oneline --abbrev-commit -S'shortest_path'`
    - Then add that filename/directory as additional option to that command

- Do you have to specify your git user name and email every time you open a new terminal?
    - No. When you 'git config' those values, they are stored in a config file. Either within current repo or with '--global' in your home directory. The latter is more convenient as it applies to all repos.
    - When you set them globally, Git remembers them for all repositories on your computer. 
    - If you set them without '--global' means you need to set them once per repository (but again not every time you open the terminal)

- in VS code after choosing select “networkx-2.6.3”. should i see a change in the bottom branch name? for me it show like im still in main, is that ok? --- nevermind i didnt read correctly and it was requesting a name for my new branch, that is why it was not changing
    - To be sure which branch you are currently on, try 'git branch' in the terminal. it will show you the branch you are in. There is a '*' shown near the branch you are already in.
     
- what is the difference between git switch and git checkout?
    - git checkout was the old way to do git switch. Git checkout is used also for other things, so git switch (and git restore) came after to avoid confusions with git checkout.
    - "Switch" is only for switching branches, simpler and safe, "Checkout" do multiple things including switch branches.

- What's the difference between git switch --create and git branch?
  - when you use `git switch --create new_name` create a new branch with the name chosen and automatically switch to that branch. however, using `git branch new_name`, create the new branch but does not switch to it.

- In the solution of the first part it suggests, after "git annotate" to "Then search for “Logic error” by typing “/Logic error” followed by Enter." im not sure where I should type “/Logic error”.
   - `git annote` should open a view that takes the whole window. Typing "/Logic error" there and pressing enter searches for "Logic error".
   - If file is short, then 'git annotate' simply prints the text to terminal. If it is long, then git starts 'less' that a provides a "browseable" view. Less takes some keys as commands. For example, `q` quits less and `/` makes it expect a word to search. One can disable the use of less _and_ search text:
       - `git annotate README.rst | grep "Logic error"`
       - That passes the output of git to program grep that filters out lines that lack the _Logic error_
       - For this one I got "grep: error”: No such file or directory"
           - Then the shell has no access to program `grep` -- not installed on your system
           - How do I download it?
   -  It says "bash: /Logic: No such file or directory"
      - You probably did not type /Logic in the "git annotate" view
        (the pager, or the "less" view, to use other terms)
        but instead in the shell. Could that be?
        - Yes, corect; nothing new opens 
          - if you did:
            1. `git grep "Logic error"`  
               then you should get that the file containing it is 
               "networkx/algorithms/threshold.py"
            2. then if you use the command
               `git annotate networkx/algorithms/threshold.py`
               you should get definitely some output in the terminal,
               but since it is very long, 
               then you should enter a view where you can go up and down 
               with the arrows - a "pager".
                   - If the pager is less, then the last line on terminal has `:` and blinking cursor
            3. There, you can search by typing `/` following by whatever you want to search ("Logic"), and press enter (and n or N to go to the next mac)
            4. Ah yes is I type after the : (after annotate) it gives me a new list and the first part is "c585bf422f      (loicseguin     2010-08-02 14:50:33 +0000       485)                print("**Logic error** in degree_correlation",i,rdi)" so not the same as the exercise, is this ok?
               - That seems ok! thanks!
               - The output is a little different from mine, but perhaps you did not switch to the branch networkx-2.6.3 branch first?

- I guess this line 'Logic error...' was removed in this commit - caba9e947a72b64d791fc3e3da5b9dbaeed067b1
  - Hm. Was it removed? Have you checked the correct branch?
  - from main, when I use 'git grep "Logic error in degree_correlation"', it doesn't return anything. Then I manually checked and found that this line was removed and not part of the main branch anymore.

- I understand we need to configure SSH key before the after lunch session. after setting up my SSH key I still get permission denied (publickey)
  - Join us in the help room? Or: make sure that you copied the ssh key (the WHOLE content of the .pub file) into github (settings -> ssh and gpg keys -> new ssh key green button -> paste in "key" field -> new ssh key button -> confirm via email or other means)
  - Solved! thank you :)

## Break: 20min exercises (until xx:00), 1hr lunch (until 14 EET, 13 CET)
First, work on the git archeology (history inspection) exercise.  Try to do what you can, future exercises don't depend on this.  You can try the optional git-bisect advanced exercise if you'd like. 
[Exercise 
- Explore basic archaeology commands ](https://coderefinery.github.io/git-intro/archaeology/#exercise)

Then take a nice lunch break.  After lunch, we are back and may do the git-bisect exercise and will show how to share code from your local code to Github, and other practical advice.


> In case, you haven't configured your Git, make sure you do before the next exercise. Here's some info on how to configure: [Configuring Git command line and editor.](https://coderefinery.github.io/git-intro/configuration/#configuration)
> We have adjusted the Notes settings some, which may prevent people from getting disconnected.  Please report any weird things you may see.

##  [Git bisect](https://coderefinery.github.io/git-intro/archaeology/#finding-out-when-something-broke-changed-with-git-bisect) 

Questions continued: 

> Note: you might have to refresh the twitch tab to get reconnected to the stream (this was necessary for me) 

> A comment on 'git bisect': it looks like a very powerful command, but you need to have "clean" commits, in which the code is working to the best of your knowledge
    
- Is it necessary to mark several commands as good/bad in the meanwhile? I mean if you're toggling between commits and you have to run your `*.py` to check, wouldn't it suffice to just point to one break-point and the next good one?!
    - The scenario is the one where you know that a commit 100 commits ago was "good", but now it is "bad", and to find a bug you would like to find the commit that "broke" the code: hopefully, the bug can be found in the (hopefully little) diff/ "git show" of that "breaking" commit. To get that commit, it is typically more efficient to use a bisection algorithm to check a few commits, rather that checking all the commits.

- How does git determine the commit number to test next? Since git doesn't really know which function you are testing, does it only get random numbers or does it actually check at differences in the exact function you are testing?
    - You mark one commit as "good" and another as "bad". It will look at which commit, in the history, is in the middle, and jump to that. Git is totally unaware of what your code does or means, it's you telling Git what to do by marking commits as "good" or "bad".

- So then one could do this manually as well. Take the one in the middle and iteratively check. The only advantage is that git autoamtically takes you to the middle commit without you having to look for the hash and doing it yourself.
    - Exactly. There is also `git bisect run testcommand` that would "test and hop" even more automatically
- Nice, thanks! :)

- how do you leave the bisect mode?
  - 'git bisect reset' (verify with "git help bisect")
  - The command above stop the basic session and return your repo to the branch and same commit you were in before you started the bisecting.
- Mic was cutting out?+1 
    - Thank you, yes hopefully fixed now. But do let us know if you encounter issues with the stream

- does bisect only works with the command line?
  - I think so. It could be that some editors/IDE implement it for you, but I am not aware of that. Also, you can still use git from the editor/IDE, and at the same time use git from the command line for these "advanced" commands
- Do I really not need SSH in VS code?
  - IIRC, VSCode itself can authenticate to github in other ways (using HTTPs or something related), but from the command line you need ssh (only when using push/pull)
- In the bisect exercise, I tried `git switch <hash>` (to get to the original commit) and that failed. Am I missing a parameter? (whereas `git checkout <hash>` worked).
  - switch works for branches, not for specific commits.
    If you do `git checkout <hash>` you end up in a "detached HEAD" state,
    which means you are not on any branch.
    `git switch` needs an existing branch as an argument
    - I believe the instructor mentioned that you could use both switch and checkout for this, but that checkout was the 'old-school' way to do it. But presumably the original commit is not available as a branch.
        - To use `git switch` to check out a commit, it requires a flag `--detach`

## [How to turn your project to a Git repo and share it](https://coderefinery.github.io/git-intro/sharing/)

### Exercise until xx:45

Exercise link: https://coderefinery.github.io/git-intro/sharing/#exercise

Goal: Create a local repository and push it to the remote at Github. Or push the repository you worked on before, e.g., recepie-book

Status: 

- done: ooooooooooo
- not trying: oooo
- major issues (please join the help room (link in email)): o


- After publishing the repository VSC asked me if i want it to periodically fetch from github repository. What's up with that? Would you recommend doing it?
    - If I understand correctly, this would help making sure that VSCode always sees an updated version of the remote branches (probably relevant in the "network/graph" view you have on the bottom left corner when source control is clicked). I'd say not worth it (fetch is not pull, so you would need to actually manually "pull" to update your local branches, right?), but it should not matter that much.
    - As said yesterday it is good practice to keep local repo in sync with the remote. Whether plain fetch is good enough, or will the pull be necessary is a followup issue _and_ with pull you may face _non-trivial merges_

- When using command line: we initialise a main branch when setting up a local repository, but then when linking to the github remote repo there's a `git branch -M main` command. Does this need to be run when the branch is already called main?
  - That command is not useful for **new** versions of Git, which use main as a default branch name. Older versions of git used **master** as a default branch name, and that command is used to change the name of the branch you are on from whatever it is (could have been master, if you had an old version of git) to "main", the now commonly accepted name for the default/most important branch
    
- When I start a project I actually begin in Github with a minimal repo (README and .gitignore). Clone it and start working there, then push changes. Is this a normal accepted approach? Or people start local and then do as in the exercise :)
  - This works fine if you don't have a local repository already. Otherwise, you need a special option to merge the unrelated histories of the remote repository and the local repository, if you have something (= some commits) in both repositories before they get connected.

- Is there a simple way to roll back if I accidently `git add .` and `git commit -m "MESSAGE"` with secrect in local repo?
  - Yes! As long as you don't push. `git reset HEAD~` takes your current branch and makes it point to the previous commit, without changing anything in the working directory. 
  - So, no history will be pushed?
    - if you do first `git reset HEAD~` (ONCE, be careful) you should be able to verify the status with `git status` and also `git log`. Then, if you push, you will push only what has been committed so far on this branch (which, since you moved the current branch back a commit, does not include the last, wrong commit). Note: `HEAD~` is an expression that for git means "the commit before the one I am on"
    - Thank you!

- When publishing the repository in private Git I get this warning "Can't push refs to remote. Try running "Pull" first to integrate your changes.". How can I publish? The options I'm given are "Open Git Log", "Show Command Output" and "Cancel".
   - It means your local branch and the remote branch you are trying to push to have diverged. so you need to sync first 'git pull', resolve any conflict (likely in your editor), and then run 'git push' to publish your commits.

- would it be possible to develop this chapter furthere? : "Is putting software on GitHub/GitLab/… publishing?".
    - What would you like to see there more?
    - How would it be publishing then? how should it be linked to Zenodo, for example?
        - Yes, adding some persistent identifier, like a DOI with Zenodo or other service of choice
    - We have more about this coming next week in reproducible research and social coding sessions.
    - GitHub has instructions on how to _link_ GitHub and Zenodo. Once done, creating a release in GitHub submits a "dataset" to Zenodo automatically (looking forward to this :))
        - this is indeed a great feature. We currently only mention this in the social coding lesson coming next week, see link below
    - Are you thinking about something like this: https://coderefinery.github.io/social-coding/software-citation/#is-putting-software-on-github-gitlab-publishing
        - I will check that.... Thanks!!!

- In VSCode, I don't see the Publish to GitHub button.
  - Do you want to join the help room? You may see a "publish branch" blue button in the source control tabs
  - if you are checking the lecture on twitch, they are showing this now on VScode. In case it helps :)

- Following the instructions for the terminal the command 'git push -u origin main' returns "fatal: 'git@github.com/MYUSER/MYREPO.git' does not appear to be a git repository. Fatal: could not read form remote repository. Please make sure you have the correct access rights and the repository exists."
  - there's a couple of issues:
    1. it should be git@github.com:MYUSER/MYREPO.git , with a : instead of a / , IIRC
        - This returns "remote origin already exists"
        - are you trying with `git remote add origin ...`?
          if so, you need another command:
          `git remote set-url origin <new-url>`
          this will change the url of the "origin" remote repository
          -    This works, thanks!
 
    3. make sure that you correctly wrote the username and the repository 
- Any security issue with using HTTP instead of SSH for git?
  - Not really. It's just that ssh can be easier to work with, since there are more tools around it - at least from the command line
  - Thank you!
 
-  Any recomendations on how to generate a license for our work code?
    - We will get to that next week Tuesday in our social coding lesson. Sneak peak: https://coderefinery.github.io/social-coding/software-licensing/
        - You asked to generate, therefore only a short note: Please always choose some already existing license, do not try to write your own :) There are wonderful tools out there to help you choose, depending on what you need.
        - ok thanks!

- When I try to upload files using the command it ask me for the user and password, but the pasword never works! i need to use the toke. why?
    - You mean, with git push? This is probably happening if you have used the https version and not the ssh version of the 
    - ahh! 0k.

- Do i always have to open a new repo in github, which i can basically do nothing from cli?

    - No, you can also start a repository entirely locally in your machine using `git init`, do all changes you want (even offline) and push your project to GitHub afterwards.

- Any commands that can work in Terminal to set 'Private/Public' status of the repo instead of manually tackle it from the web browser?
    - "Private" or "public" is not something you can set with 'git', it is a github specific feature. From the command line, you could use a github command line app, probably, to do github-specific things. 
    - So you can change the visibility of the GitHub repository using `gh repo edit --visibility private/public`

- I have a follow-up question on rolling back an accidental `git add .` and `git commit -m "MESSAGE"`. If you use `git reset HEAD~`, do you lose the changes you made (but did not commit)? Or does it simply (and essentially) reverse the commands `git add .` and `git commit -m`, meaning I would still have the changed, untracked files?
    - Hi, I asked the questioin, and the change was still there, just back to the status before `git add`. So, all files are there still.
    - Amazing! Thanks! :smiley:
    - The 'reset' has _mode_ options: `--soft`, `--hard`, etc
      - `--soft`: changes only where the branch points to, but the changes you had committed stay "added" (you still see them staged when you do "git status"), files on disk are not changed 
      - `--mixed`: the default, the branch is moved, the changes you committed are not "added" any more (so you have to "git add" them again, if you so wish), files on disk are changed
      - `--hard`: the nasty one. This changes also the files on disk. This completely deletes what you have done. Good if you really want to start from scratch because you did something you really want to forget. 


## Break until XX:10

## Now here: https://coderefinery.github.io/git-intro/sharing/#is-putting-software-on-github-gitlab-publishing
> More on this topic coming up in Day 4 (Tuesday next week) in social coding lesson


Questions continued:

- What if we published our source code as the supplementary material of a journal paper first? What is recommended to publish the same repository on GitHub later? What is the best practice for this?
    - Good question. This may also depend on the journal you are publishing. They may have their own requirements. Some Software Journals may also ask for a Git(Hub/Lab/...) link in addition to a DOI.  
    - Leaving this open for anyone who wants to share own experience/good practices: 
        - I'm interested in this as well. It would be great to also hear teacher's perspectives and experiences on this, next weeks sessions maybe?
        - We will definitely circle back to this during social coding lesson as well. (Tuesday next week)
        - INTERESTING TOPIC!!!
        - If you want to make sure you are allowed to reuse material from an article you can publish the artcle with a clear open license which permits reuse of the content. If the article doesnt have a permitting license it would be best to ask the publisher.
    - Github and journals/Zenodo for archiving data&code have different purposes: Github/Gitlab/etc. is good for collaborating.  Journal SIs/Zenodo/etc. has a snapshot that will be available indefinitely (Github could close your account or change its practices, in theory).

    
- So if you use GitHub you can get a DOI by using zenodo. Is there also a way to get a DOI if you use GitLab or another service?
  - You can always do it manually too. By creating a release of your code, download the code eg as zip file and upload it to Zenodo. 
  - Sounds complicated. Would it be easier linking zenodo and github? 
      - Depends on your preferences. It is not super complicated, just a bit of work. There are some workarounds mentioned when googling the issue with GitLab, scripts one can run etc. GitHub certainly makes the process easier for you. 

- I want to ask about `git pull`, sometimes it leads to conflicts on my local repo: how to deal with conflicts between local and remote when collaborating with other people on the same Git repo?
  - There's a number of ways to reduce conflicts:
    - merge often. You might get conflicts, but they will be smaller and far easier to work out. This is by far the best way to work, but this requires that you are confident you can merge often without causing problems. This typically requires automated testing... see next week! > Okay, thank you!
    - use small files. If you reorder code in a file and commit that on your branch, someone changes it on another branch without reordering, merge will very likely cause a conflict. If you had small files instead, this would not generate a conflict.
  - I would not say "same git repo" as everyone have their own local git repo, and then there is the repo in GitHub via which the changes are "communicated". Rather a "same project", isn't it?
    - It happened that multiple people pushed differnt changes to the Git repo at the same time.
      - This happened on different branches, right? At some point all these branches should be "merged", probably one after another, into "main".
        Is this what happened? 
    - Maybe we only worked on "main" branch, which may not be a good idea.
        - I was going to comment this, I'd say one good practice is having different branches when having several people working on the same repository. That said, that doesn't avoid conflicts all together because you will probably want to merge back the changes to "main" at some point. However, it is easier to work this way, since you will have less or no conflicts in your usual workflow and handle all conflicts when merging back to "main". It is nice to handle this through a pull request, since you can review all changes and even get comments from other people involved before making the merge. Tomorrow will see more of this :)
    - Thank you!
- How do you enter a body message for a commit from terminal? I usually do for instance, git commit -m "fix:short message". Cuz from the GUI you have the option to put a short message and then a description.
    - Do not give the `-m "message"`  on the command. Git should open a text editor for you 
    - Make sure your editor is configured correctly
      (see `git config --list`, check for `core.editor`)
      `git config --global core.editor <editor-I-am-confortable-using>`,
      for example use `nano` for `editor-I-am-comfortable-using`
      (if you entered vim by mistake, type `ESC`, then `:q!` and ENTER to exit)
- why sould we use command line and not just the VS code?
  - Use what you are comfortable with! But keep in mind: the command line interface of git will be always available, VSCode not necessarily.
  - Understood!
  - see also https://en.wikipedia.org/wiki/Lindy_effect. The shell has a long tradition, VSCode is a convenient tool that might stop being convenient at some point. Also, there are things that you simply can't do in VSCode. 
  - Nice point. Thanks!


## [Practical advice](https://coderefinery.github.io/git-intro/level/) 

Questions continued: 

- Speaking of README.md, any remarks on what a good README should look like/contain? generally.
   - In exactly a week there's going to be a lesson about documentation!
    - You are all asking super good questions. ^


## How are you using Git? Let us know! 

... what do you want us to talk about?

- I may or may not have a project that has been under RCS, CVS, Subversion, and Git ... (but not in GitHub)
  Both for writing tools and utilities for research, but also to store/record configuration management system's site-specific config

- I am using it to publish image analysis pipelines for the users of our microscopy core facility (to keep track of development, fix bugs amnd distribute the latest version to the users in an easy way). I just learnt yesterday about tags, releases and integration with Zenodo, so will use it when referring to the code in methods (to generate a DOI). So far I was just using the GitHub repo :)

- I'll be using it for smaller personal projects (on the data analysis side of things), as well as probably contribute to larger software projects.

- I mostly used it to for university group projects to share a code across my group. However, I wanted to start use it on a daily to prevent haveing 100 files called My_project_final_final_reallyfinal.py as well as keep neat documnations all of my code for my students.

- I'm now trying to use git for Obsidian(note taking program) to share files between mobile phones and computers(had file collisions when using dropbox, mega etc. I had files myhisteriously disappearing.). This is actually I great idea (I was using OneDrive haha)!
    - Oh this sounds very useful! Is it difficult to set up? I just started with obsidian and was wondering how to share it across my devices.
        - I have a hard time finding mobile apps that can pull uppdates automaticaly. Still new to me. I would like to automate as much as possible.
            - thanks a lot for mentioning it, I'll definitely try this :)
            
- Mostly for putting my reserch outputs, and codes/scripts I have used to do/create sth, so that others can follow my footsteps. Also for publishing articles and so on that now is sorta mandatory.

- I develop and implement methods for analysis of experimental/simulation data, which has produced a growing body of code which isn't terribly organized or accessible to anyone else who might become involved with the work in the future. I'm hoping that integrating git in my workflow will help improve this situation!
  - Git is not a magical tool that can tidy up code, BUT it's definitely a necessity to have a tidy project.
      - and it helps you develop the habit of keeping your code tidier, documented, etc. Even if it is just a little bit more than now, that is always a win (talking from personal experience)
      - I think that just the obligation of writing commit messages has really helped me reflecting about what I have done

- I use git for everything, even for sensitive data (personal data), but use `git crypt` to encrypt it. Wondering whether it is something that (other) people would find useful too...
-Does sensitive data get troubles in the future? maybe something in small letters in the copyright agreement with github?

- I am stariting to use it for publishing a web page from my results and also publish the code used in the analysis.
  - We'll talk about something similar next week in the documentation session!
  - GREAT!!


---

## [What to avoid](https://coderefinery.github.io/git-intro/what-to-avoid/) is being discussed on stream 

Questions continued: 

- Wont' rebasing delete the selected commits from the public history? For instance, if I don't want to show merge branch develop/main (as it sometimes is just a filler commit), I usually rebase and then force push to remote. Would it still be possible to find that deleted commit after rebase+force-push on the remote?
  - force push is always dangerous. A trick you can use to keep also the old commits is to create a new "bookmark" branch at the old location/commit, and still force push on the old branch. The "force-pushed" branch will be "overwritten", but the commits will still be accessible in the "bookmark" branch.
  - Locally, you can still recover the old commits before the rebase using `git reflog` for the branch you're doing surgery on
  - I think yes, there is a possibility that the old versions are on the remote.  Git has some garbage-collection that will periodically delete old, unreference commits (I've once heard something like two weeks?), and Github has the same.  It is definitely something you should check more, if it's important.

- If in my script I have references to local paths/keys that are stored in some config files I would have to add that to the git ignore. However this would probably make the script not work for someone else as the file would be missing: how do you fix that?
  - Sometimes I include a default file that is committed, or template file that has to be copied and edited before it can run.  I might adjust the code so that it it can read from multiple conf files: the default commited, plus local one.  It's a design decision, also to see if there are any defaults that would work for everyone.
  - Your scripts need to be changed so that they can be used with input that one can specify - i.e., made more versatile, e.g. with command line arguments. But it is good to still add some examples, or some dummy data that can be used. 

- Continuing with the previous question... it will be like including some data, or a part of it in the repo, so the code would work for someone else?
  - you can still do that. Large data might be better stored somewhere else though, and you can add a link/instruction on how to get it. It can be good to store some sample/dummy data so show how your code can be used.
  - But I would really suggest making your script flexible enough that one can specify separately (e.g. from the command line) what data to operate on. 


---

## Feedback for Day 2 of CodeRefinery workshop

:::success
- Today, we covered everything in the schedule: We moved from the GitHub web interface to local computer and experienced the power of working locally, Inspecting history, Sharing work, Practical advice, What to avoid.
- Day 3 is when we will collaborate together and we will send you detailed instructions on how to do that via email later today.
- For day 3, If you plan to do the exercises please make sure you have:
   - a working git installation in your computer (e.g. with VS Code or with the shell terminal, see instructions at https://coderefinery.github.io/installation/)
   - GitHub account

Twitch will store this video for 7 days, and hopefully it will be on YouTube by the time that expires.

:::

### Today was (vote for all that apply):
too fast:ooooooo
too slow:o
right speed:oooooooooooo
too slow sometimes, too fast other times: ooooo
too advanced:ooooooo
too basic:o
right level:oooooooooooooo
I will use what I learned today:oooooooooooooooooooo
I would recommend today to others:oooooooooooooo
I would not recommend today to others:


### One good thing about today:
- git bisect seems like a practical new feature <3
    - Indeed
- the idea of checking the "old version" of the code is really cool
- yes, `git bisect` is really useful!
- Interesting topics, intersting discussion, Nice to meet VS code..
- I understood my mistake about git in my ongoing project at work
- I appreciate that you provide instructions for several different ways of working with git, such as in RStudio


### One thing to improve for next time:
- More "unknown" functions(i.e. bisect) that mostly are not used that can be practical.
- the instructions in the github.io is VERY CONFUSING, like I do understand i have to find a hash for certain version, but i am really unsure where is a right place to find the hash `git log` or simply `git show`, then in answer `git switch --create just-before 90544b4fa~1` just come out of no where, and I was checking the has in `git show` the hash before `90544b4fa` is not easy to spot, and I am not even sure that is right
- On Gitlab, one can actually push a local git repo to remote repository without first creating it online. So, maybe some demo using Gitlab?
- For complete beginners there is quite a gap between yesterday and today's content (at least this morning), installation might be the biggest issue
- Organization previous to the meeting?
- Sometimes during the check of the exercise, nobody followed certain points (like the graphs); overall the command view was a bit confusing and there could be more time spent on this; also I missed a file filled with some commands that Blazej had opened 
- It was hard to follow the whole command part; and the guide for VS was incomplete
- Some exercises could not be done in VS code, so switching quickly to command line was difficult, as I had not set it up 
- More practical exercises would be better to remember the commands discussed today
- The introduction to exercises went too fast sometimes. For a beginner, it was not clear where to do which things, especially the exercise right before lunch was not presented clearly enough. (+1)
- More examples of "real life" workflows/cases



### Any other feedback? General questions?
- Are we going to learn how to use Git for Jupyter notebooks in this workshop in the upcoming days? o
    - We used to have a full lesson on Jupyter notebooks, of which you can find the materials here: https://coderefinery.github.io/jupyter/
        - These also have a section on Git for Jupyter: https://coderefinery.github.io/jupyter/version-control/
        - Thanks a lot! I will go through them.
            - Since it was part of the workshop you can also find the recording of this lesson on our YouTube channel, search for CodeRefinery, and find any of the earlier workshops playlists.
                - Found it. Kiitos! For others - https://youtu.be/FGqz5_Do3Og?si=yWlCizipVMTG4KZ2
- Thanks for live help (Zoom) <3
- I did the optional exercises on staging, and I feel like this was really important for good commits so I would love to have it in the main session.
- will we see how to use git through an hpc environment or are there any good material elsewhere you could recommend?
- THANK YOU!!!.
