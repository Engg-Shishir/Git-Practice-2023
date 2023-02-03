<div style="background-color:MediumVioletRed;text-align:center;color:white;">
  <strong><h2>Create Working Folder </h2></strong>
</div>

> `Git Practice -2023`



+ Open terminal fand get inside of  Git Practice -2023

    ```html
        For my case this was happened
        + C:\Users\shish> cd Onedrive
        + C:\Users\shish\OneDrive> cd Desktop
        + C:\Users\shish\OneDrive>Desktop> cd Git practice - 2023
        + C:\Users\shish\OneDrive\Desktop\Git practice - 2023>
    ```

<br><br><br>
<div style="background-color:MediumVioletRed;text-align:center;color:white;">
  <strong><h2>Inialize folder as a git folder : </h2></strong>
</div>

<img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="30px" style="margin-top:10px;"> `git init`

>  Now a .git folder is created inside working folder






<br><br><br>
<div style="background-color:MediumVioletRed;text-align:center;color:white;">
  <strong><h2>Check Status </h2></strong>
</div>

+ Create a `Readme.md` file : `touch Readme.md`
  + If you find this error : touch is not recognized as an internal or external command, operable program or batch file. Then run `npm install touch-cli -g` then run `touch Readme.md`

<img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="30px" style="margin-top:10px;"> Check git status : `git status`
  + you will see ---------------------
  ```html
    > On branch master
    > No commits yet
    > Untracked files: Readme.md
    > nothing added to commit but untracked files present (use "git add" to track)
  ```


<br><br><br>
<div style="background-color:MediumVioletRed;text-align:center;color:white;">
  <strong><h2>Working Dir to Staging Area</h2></strong>
</div>

+ Update all file into `Staging Area` It is also called `Index` <br>
<img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="30px" style="margin-top:10px;">Run : `git add .`   OR `git add fileNameWithExt`. <br>
Now git `track `all of changes inside the folder file.The index is the “staging area” in your Git workflow.

+ Again check git status : `git status`
   + you will see ---------------------
   ```cmd
    > On branch master
    > No commits yet
    > Changes to be committed: Readme.md
   ```

<br><br><br>
<div style="background-color:MediumVioletRed;text-align:center;color:white;">
  <strong><h2>Unstage Specific File</h2></strong>
</div>

<img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="30px" style="margin-top:10px;"> If you want to unstage specific file Run : `git restore --staged filenameWithextention`
  + Unstage `Readme.md` file : `git restore --staged Readme.md` or `git reset`
  + Check status : `git status`
  + you will be show ---------------
  ```html
    On branch master

    No commits yet

    Changes to be committed:
            new file:   Readme.md

    Changes not staged for commit:
            modified:   Readme.md  
  ```
+ Again back to staging area : `git add .`



<br><br><br>
<div style="background-color:MediumVioletRed;text-align:center;color:white;">
  <strong><h2>Enter to Loacl Repository Area from Staging Area</h2></strong>
</div>

<img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="30px" style="margin-top:10px;"> Run :  `git commit -m"Create Readme File For Document's writing"`




+ Check all kinds of Commit inforamtion in Local Repository<br>
<img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="30px" style="margin-top:10px;"> Run for details info :  `git log-a` <br>
<img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="30px" style="margin-top:10px;"> For shorter Info `git log --oneline`
    + You will see ------------------
    ```html
        ead152e (HEAD -> master) Create Readme File For Document's writing
    ```
    This message tell us that, this commit is created inside `master` branches & now we are working in master branches`(HEAD -> master)`.









<br><br><br>
<div style="background-color:MediumVioletRed;text-align:center;color:white;">
  <strong><h2>Git reset</h2></strong>
</div>

+ Create some file and Staging them : `git add .`<br>
  <img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="30px" style="margin-top:10px;">  Now run : <strong style="color:red;">git reset</strong> OR <strong style="color:red;">git reset --mixed</strong>  <br> This command bring back all `staging file` into `working directory` 



<br><br><br>
<div style="background-color:MediumVioletRed;text-align:center;color:white;">
  <strong><h2>Git reset --hard</h2></strong>
</div>

+ Now update something in a file which alredy under commited. Suppose in `Readme.md ` file i write `I love bangladesh`
    + Check status : 
    ```html 
    On branch master
    Changes not staged for commit:
            modified:   Readme.md
    ```
    <img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="30px" style="margin-top:10px;"> Now run : <strong style="color:red;">git reset --hard</strong> and you will see the updated text is not available in the file. that mean's `I love Bangladesh` is no loger available in `Readme.md` file.                 
    A hard reset will delete any new files that were added to the index, and undo any updates or changes made to any files that were part of the repository when the last commit occurred. This command typically fulfills the need for a git uncommit command.<br><br>



<br><br><br>
<div style="background-color:MediumVioletRed;text-align:center;color:white;">
  <strong><h2>Git reset --soft head^^</h2></strong>
</div>

+ Create a file `check.md`

    <img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="30px" style="margin-top:10px;"> Now run : <strong style="color:red;">git reset --soft head^^</strong> <br>
    + Check status : `git status `You can see -------------------
        ```html
        On branch master
        Changes to be committed:
                modified:   Readme.md
                new file:   Secondfile.txt
                new file:   thirdfile.txt

        Untracked files: check.md
        ```
    + Chek commit details : `git log --oneline` & OVserbe result 
    ```html
    ead152e (HEAD -> master) Create Readme File For Document's writing
    ``` 
    That means, this command bring back all file under `last commit` to` staging area` without deleteing or changing something. Also others all of file working procedure remain same.<br>

<br><br><br>

<div style="background-color:MediumVioletRed; ; text-align:center;">
  <strong><h2>Git Branching</h2></strong>
</div>
<span style="color:gray;">In Git, a branch is a new/separate version of the main repository. Branches allow you to work on different parts of a project without impacting the main branch. When the work is complete, a branch can be merged with the main project.

In Git, a branch is a separate line of development that allows you to work on different features or bug fixes in parallel. When a branch is created, it is a copy of the main branch (usually "master"), and changes made to the branch do not affect the master branch until the branch is merged back into it. By using branches, multiple people can work on different parts of a project simultaneously, without causing conflicts.
</span>

> Create a branch : `git branch NewBranch`

> Check all branches : `git branch` .You can uderstand which branch is under development by (*) pointer.

> Switch branch : `git checkout BranchName` Or 

> Directly switched when branch is created by :  `git checkout -b NewBranch`

> Delete a Branch : `git branch -d new` . To do this first checkout to `master `branch. <br>

<br><br><br>

<div style="background-color:MediumVioletRed;text-align:center;color:white;">
  <strong><h2>Branch Merging</h2></strong>
</div>

> Switch to master branch : `git checkout master`

> Merge the current branch (master) with emergency-fix : `git merge emergency-fix`

<br><br><br>

<div style="background-color:MediumVioletRed;text-align:center;color:white;">
  <strong><h2>Merge Conflict / Git Conflict</h2></strong>
</div>
<span>A Git conflict occurs when two or more branches have made changes to the same part of a file, and Git is unable to automatically merge those changes. Git will mark the conflict in the file and require manual intervention to resolve it before the merge can be completed. Resolving the conflict involves deciding which changes to keep and which changes to discard, and then updating the file accordingly. Conflicts can be resolved using Git command line tools or other merging tools.
</span>

>  The process to resolve a Git conflict is as follows: 
+ Identify the conflict: Git will mark the conflict in the file with special conflict markers and inform you that a conflict has occurred.
+ Open the file with the conflict: Open the file with a text editor to view the conflicting changes.
+ Decide which changes to keep: Review the conflicting changes and decide which changes to keep and which changes to discard.
+ Update the file: Remove the conflict markers and any changes that should be discarded. Update the file with the desired changes.
+ Commit the changes: Stage the file and make a commit to resolve the conflict. This will allow you to merge the branches.
+ Repeat as needed: If there are multiple conflicts, repeat the process for each one.
> Note: It is always recommended to backup your code before resolving conflicts.

<br><br><br>
<div style="background-color:MediumVioletRed;text-align:center;color:white;">
  <strong><h2>.GitIgnore</h2></strong>
</div>
<span>When you make commits in a git repository, you choose which files to stage and commit by using git add FILENAME and then git commit. But what if there are sWhen you make commits in a git repository, you choose which files to stage and commit by using git add FILENAME and then git commit. But what if there are some files that you never want to commit? It's too easy to accidentally commit them (especially if you use git add . to stage all files in the current directory). That's where a .gitignore file comes in handy. It lets Git know that it should ignore certain files and not track them.ome files that you never want to commit? It's too easy to accidentally commit them (especially if you use git add . to stage all files in the current directory). That's where a .gitignore file comes in handy. It lets Git know that it should ignore certain files and not track them. 
</span>

> How Works ?

Here's how it works. A .gitignore file is a plain text file where each line contains a pattern for files/directories to ignorHere's how it works. A .gitignore file is a plain text file where each line contains a pattern for files/directories to ignore. Generally, this is placed in the root folder of the repository, and that's what I recommend. However, you can put it in any folder in the repository and you can also have multiple .gitignore files. The patterns in the files are relative to the location of that .gitignore file.e. Generally, this is placed in the root folder of the repository, and that's what I recommend. However, you can put it in any folder in the repository and you can also have multiple .gitignore files. The patterns in the files are relative to the location of that .gitignore file. 

> Example :------------------------------------<br> 
    logs/<br>
    *.log <br>
    !example.log<br>
    logs/<br>
    !logs/example.log<br>





<div style="background-color:Indigo;text-align:center;color:white;">
  <strong><h2>Push / Pull -- Github</h2></strong>
</div>

+ Check is any connection between Local-repository & Github(remote repository) : `git remote -v` If any connction is found it gives a URL.Otherwise nothing is return.
+ Create connection between them(Local Repo & Remote Repo) : `git remote add origin https://github.com/Engg-Shishir/Git-Practice-2023.git`  (Here `origin` represent remote repository connection URL ). Next time you can use `origin` as a referances of connection URL(https://github.com/Engg-Shishir/Git-Practice-2023).
   + Now again check : `git remote -v` 

+ Change `master` brance name as a `main` branch if you want : `git branch -M main`. But this is not necessary. `master` is much preferable than `main`

+ Now PUSH your branch in remote repository : `git push origin master`. Everytime this command PUSH, local repository master branch in remote origin(https://github.com/Engg-Shishir/Git-Practice-2023). That means if any new commited are created and want to push, you should run this command everytime.

  + You can also run : `git push -u origin master`. It's established permanent connection between origin and localBranch. That's why to push some commit just run : `git push`.No need to mention `origin master`.















<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

<div style="background-color:MediumVioletRed;text-align:center;color:white;">
  <strong><h2>MediumVioletRed</h2></strong>
</div>
<div style="background-color:DeepPink;text-align:center;color:white;">
  <strong><h2>DeepPink</h2></strong>
</div>
<div style="background-color:OrangeRed;text-align:center;color:white;">
  <strong><h2>OrangeRed</h2></strong>
</div>
<div style="background-color:DarkOrange;text-align:center;color:white;">
  <strong><h2>DarkOrange</h2></strong>
</div>
<div style="background-color:Orchid;text-align:center;color:white;">
  <strong><h2>Orchid</h2></strong>
</div>
<div style="background-color:Fuchsia;text-align:center;color:white;">
  <strong><h2>Fuchsia</h2></strong>
</div>
<div style="background-color:Magenta;text-align:center;color:white;">
  <strong><h2>Magenta</h2></strong>
</div>
<div style="background-color:MediumOrchid;text-align:center;color:white;">
  <strong><h2>MediumOrchid</h2></strong>
</div>

<div style="background-color:RebeccaPurple;text-align:center;color:white;">
  <strong><h2>RebeccaPurple</h2></strong>
</div>

<div style="background-color:BlueViolet;text-align:center;color:white;">
  <strong><h2>BlueViolet</h2></strong>
</div>

<div style="background-color:DarkViolet;text-align:center;color:white;">
  <strong><h2>DarkViolet</h2></strong>
</div>

<div style="background-color:DarkMagenta;text-align:center;color:white;">
  <strong><h2>DarkMagenta</h2></strong>
</div>

<div style="background-color:Purple;text-align:center;color:white;">
  <strong><h2>Purple</h2></strong>
</div>

<div style="background-color:Indigo;text-align:center;color:white;">
  <strong><h2>Indigo</h2></strong>
</div>

<div style="background-color:SeaMediumVioletRed;text-align:center;color:white;">
  <strong><h2>SeaMediumVioletRed</h2></strong>
</div>

<div style="background-color:DarkMediumVioletRed;text-align:center;color:white;">
  <strong><h2>DarkMediumVioletRed</h2></strong>
</div>

<div style="background-color:DarkCyan;text-align:center;color:white;">
  <strong><h2>DarkCyan</h2></strong>
</div>

<div style="background-color:Teal;text-align:center;color:white;">
  <strong><h2>Teal</h2></strong>
</div>



<div style="background-color:Navy;text-align:center;color:white;">
  <strong><h2>Navy</h2></strong>
</div>

<div style="background-color:MidnightBlue;text-align:center;color:white;">
  <strong><h2>MidnightBlue</h2></strong>
</div>



<div style="background-color:Maroon;text-align:center;color:white;">
  <strong><h2>Maroon</h2></strong>
</div>

<div style="background-color:DarkSlateGray;text-align:center;color:white;">
  <strong><h2>DarkSlateGray</h2></strong>
</div>