+ Create a Folder = Git Practice -2023<br>
+ Open terminal fand get inside of  Git Practice -2023

    ```html
        For my case this was happened
        + C:\Users\shish> cd Onedrive
        + C:\Users\shish\OneDrive> cd Desktop
        + C:\Users\shish\OneDrive>Desktop> cd Git practice - 2023
        + C:\Users\shish\OneDrive\Desktop\Git practice - 2023>
    ```
+ Inialize folder as a git folder : <strong style="color:red;">git init</strong> 
   ```html
    Now a .git folder was created
   ```
+ Create a `Readme.md` file : `touch Readme.md`
  + If you find this error : touch is not recognized as an internal or external command, operable program or batch file. Then run `npm install touch-cli -g` then run `touch Readme.md`

+ Check git status : `git status`
  + you will see ---------------------
  ```html
    > On branch master
    > No commits yet
    > Untracked files: Readme.md
    > nothing added to commit but untracked files present (use "git add" to track)
  ```

+ Update all file into `Staging Area` : `git add .`. Now git `track `all of changes inside the folder file.
+ Again check git status : `git status`
   + you will see ---------------------
   ```cmd
    > On branch master
    > No commits yet
    > Changes to be committed: Readme.md
   ```
+ If you want to Unstage file : `git reset --filenameWithoutExt`
  + Unstage `Readme.md` file : `git reset --Readme` or `git reset`
  + Check status : `git status`
  + you will be show ---------------
  ```html
    On branch master

    No commits yet

    Changes to be committed:
    (use "git rm --cached <file>..." to unstage)
            new file:   Readme.md

    Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git restore <file>..." to discard changes in working directory)
            modified:   Readme.md  
  ```

+ git log --oneline
