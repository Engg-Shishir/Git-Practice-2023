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

+ Update all file into `Staging Area` : `git add .` OR `git add fileNameWithExt`. Now git `track `all of changes inside the folder file.
+ Again check git status : `git status`
   + you will see ---------------------
   ```cmd
    > On branch master
    > No commits yet
    > Changes to be committed: Readme.md
   ```
+ If you want to unstage specific file Run : `git restore --staged filenameWithextention`
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
+ Now go to `Local Repository` from `Staging Area` ::::::::::: `git commit -m"Create Readme File For Document's writing"`
  + You will see -------------------------------
  ```html 
    [master (root-commit) ead152e] Create Readme File For Document's writing
    1 file changed, 54 insertions(+)
    create mode 100644 Readme.md
  ```
+ Check all kinds of Commit inforamtion in Local Repository: `git log-a` OR, For shorter Info`git log --oneline`
    + You will see ------------------
    ```html
        ead152e (HEAD -> master) Create Readme File For Document's writing
    ```
    This message tell us that, this commit is created inside `master` branches & now we are working in master branches`(HEAD -> master)`.

+ Create some new file.Example : `Secondfile.txt` &  `Thirdfile.txt`<br>
  + Stage this file. `git add .`
  + check status. You will see --------------------
  ```html
  On branch master
  Changes to be committed:
        modified:   Readme.md
        new file:   Secondfile.txt
        new file:   Thirdfile.txt
  ```
  + Unstage last file : `git restore --staged Thirdfile.txt`
  + Check status : 
  ```html
    On branch master
    Changes to be committed:
            modified:   Readme.md
            new file:   Secondfile.txt

    Untracked files: thirdfile.txt

  ```
+ Commit all of changes : `git commit -m"Some git comands prictice done"`
  +  Check status `git status`
  ```html
    On branch master
    nothing to commit, working tree clean
  ```
  +  Check commit's details `git log --oneline`
  ```html
    65fb31e (HEAD -> master) Some git comands prictice done
    ead152e Create Readme File For Document's writing
  ```

+ Now update something in a file which alredy under commited. Suppose in `Readme.md ` file i write `I love bangladesh`
    + Check status : 
    ```html 
    On branch master
    Changes not staged for commit:
            modified:   Readme.md
    ```
    + Now run : <strong style="color:red;">git reset --hard</strong> and you will see the updated text is not available in the file. that mean's `I love Bangladesh` is no loger available in `Readme.md` file.



  + First
  