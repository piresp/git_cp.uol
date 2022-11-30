# git_cp.uol

#### ID VERIFY

``` git config --global user.name "yourname" ```  
``` git config --global user.email "your@email.com" ```  
``` git config --global --list ```  

#### CLONING REPOSITORY

``` git clone https://github.com/piresp/git_cp.uol.git ```

#### ADDING FILE

For an expecific file: ``` git add "name" ```  
For all files in folder: ``` git add . ```  
Update any file moved, renamed or deleted:  ``` git add -A ```  

#### GIT COMMIT

Simple commit: ``` git commit -m "the name of commit" ```
Commit with description: ``` git commit -m "the name of commit" -m "commit description" ```


#### GIT PUSH

``` git push origin main ```
  
**origin** refers to the GitHun copy of our repository  
**main** refers to our default and only branch in the repository  


#### CHANGE BRANCH

``` git branch -m "name" ```


#### GIT INIT

Creating a new folder: ``` git init "repository_name" ```  
For an existant folder: ``` git init ```  


#### GIT PULL

Up-to-date repository: ``` git pull origin main ```  


#### UNDO CHANGES

After git add: ``` git reset HEAD "file_name" ```  
After Commit: ``` git checkout -- "file_name" ```  


#### COMMIT LOGS

show all commits ``` git log --oneline --graph --decorate ```  
set a range to see commits ``` git log id...id ```  
filter by day ``` git log --since="3 days ago" ```  
see history of a file ``` git log --follow -- "file_name" ```  
see specific commit ``` git show id ```  

#### GIT ALIAS

``` git config --global alias.command_name "name of the full command" ```

Example:  

``` git config --global alias.hist "log --all --graph --decorate --online" ```  
``` git hist ```  

You can also change or create the **alias** on .gitconfig.  
