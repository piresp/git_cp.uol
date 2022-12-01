# git_cp.uol

## INDEX

- [ID VERIFY](#1)
- [CLONING REPOSITORY](#2)
- [ADDING FILE](#3)
- [GIT COMMIT](#4)
- [GIT PUSH](#5)
- [CHANGE BRANCH](#6)
- [GIT INIT](#7)
- [GIT PULL](#8)
- [UNDO CHANGES](#9)
- [COMMIT LOGS](#10)
- [GIT ALIAS](#11)
- [IGNORING UNWANTED FILES](#12)
- [GIT COMPARE](#13)
- [BRANCHING](#14)
- [MERGING BRANCHES](#15)

-------------------------------

<a name="1"></a>
#### ID VERIFY

``` 
git config --global user.name "yourname" 
```
``` 
git config --global user.email "your@email.com" 
```  
``` 
git config --global --list 
```  
<a name="2"></a>
#### CLONING REPOSITORY

``` 
git clone https://github.com/piresp/git_cp.uol.git
```


<a name="3"></a>
#### ADDING FILE

For an expecific file: 
``` 
git add "name" 
```

For all files in folder: 
``` 
git add . 
```

Update any file moved, renamed or deleted:  
``` 
git add -A 
```


<a name="4"></a>
#### GIT COMMIT

Simple commit: 
``` 
git commit -m "the name of commit" 
```

Commit with description: 
``` 
git commit -m "the name of commit" -m "commit description" 
```


<a name="5"></a>
#### GIT PUSH

``` 
git push origin main 
```
  
**origin** refers to the GitHun copy of our repository  
**main** refers to our default and only branch in the repository  


<a name="6"></a>
#### CHANGE BRANCH

``` 
git branch -m "name" 
```


<a name="7"></a>
#### GIT INIT

Creating a new folder: 
``` 
git init "repository_name" 
```  

For an existant folder: 
``` 
git init 
```  


<a name="8"></a>
#### GIT PULL

Up-to-date repository: 
``` 
git pull origin main 
```  


<a name="9"></a>
#### UNDO CHANGES

After git add: 
``` 
git reset HEAD "file_name" 
```

After Commit: 
``` 
git checkout -- "file_name" 
```


<a name="10"></a>
#### COMMIT LOGS

show all commits:
``` 
git log --oneline --graph --decorate 
```

set a range to see commits:
``` 
git log id...id 
```

filter by day:
``` 
git log --since="3 days ago" 
```

see history of a file: 
``` 
git log --follow -- "file_name" 
```

see specific commit: 
``` 
git show id 
```  


<a name="11"></a>
#### GIT ALIAS

creating alias:
```
git config --global alias.command_name "name of the full command" 
```

Example:

``` 
git config --global alias.hist "log --all --graph --decorate --online" 
```

``` 
git hist 
```  

You can also change or create the **alias** on .gitconfig.
  
Example:  
  
``` 
  [alias]
      hist = log --all --graph --decorate --oneline
```


<a name="12"></a>
#### IGNORING UNWANTED FILES

Git Ignore Pattern Examples:

Specific File:
``` 
MyFile.ext
```

File Pattern:
``` 
*.ext
```  

Folder:
``` 
my-folder/
```

<a name="13"></a>
#### GIT COMPARE

Seeing the difference between workflow and last commit:
```
git diff HEAD
```

Comparing the stage area with the last commit:
```
git diff --staged HEAD
```

Seeing the difference in just one file:
```
git diff -- file_name
```

Comparisons between commits, we use two id parameters:
```
git log --oneline
```
```
git diff ae6f872 HEAD
```

"HEAD^" means HEAD - 1
```
git diff HEAD HEAD^
```

Comparisons between two branches:
```
git diff main origin/main
```


<a name="14"></a>
#### BRANCHING

Active branch will appear with a green highlight, 

List all branches, local and remote:
```
git branch -a
```

Creating new branch
```
git branch mynewbranch
```

Rename branch
```
git branch -m mynewbranch newbranch
```

Delete branch ( you can't delete a branch you're currently on! )
```
git branch -d newbranch
```

Switching branch
```
git checkout mynewbranch
```


<a name="15"></a>
#### MERGING BRANCHES

Wen inside a branch, like main, after make some work outside in another branch named as **newbranch** for exemple, we can comeback to the main branch and merge it, just follow my steps :)
```
git checkout main
```
```
git merge newbranch
```

We can also merge branches without associate it in log ( no fast forward )
```
git merge newbranch --no-ff
```

