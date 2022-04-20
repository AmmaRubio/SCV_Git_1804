# Git Instruction 
![GIT logo](th.jpg)
## Working with Git

At the beginig use terminal to find out which version of git you have, to do so, in terminal write "git --version"
If you have git installed, zou will be displyed with a message that contains the current version of git, otherwise an error will occur. 

## Getting Git
Dowload Latest version of Git from: https://git-scm.com/downloads. 
Download with default settings 

## Setting up Git
When you first use it you need to introduce yourslef. 
For this use terminal and following commands:

* **git config --global user.name"Your Name"**
* **git config -- global user.email"your@mail.com"**


## Initializing repository 

In order to create __*repository*__ - *folder that has version control functionality*, 
```
1. open desired folder in the terminal (by command cd)
2. write command line git init
```
## Commiting, etc.
How to track changes and create commits: 
1. Firstly after changes were made to the document, it should be saved with `ctrl+s`
2. After changes in repository can be checked with command  `git status` 
3. In roder to add them to commit use command ` git add file_name`
4. At the end commit all *added* changes with command `git commit -m"message"`

## History of commits
* to display the history of all commits use command 
```
git log
```
* To display the history of all commits in graphical way:
```
git log --graph
```
* To find difference between current and last commit 
```
git diff
```

## Navigation in between commits
if you want to go from one branch to another or if you want to go to some specific commit use `git checkout commit_number`

_Example_:
```
git checkout bce480492
```
 
This command does not allow to make changes to the commited file.
To continue the Work on the file use command: `git checkout master`

## Ignoring files
Usualy large files, such as images are ignored in git (not commited), to ignore file: 
1. create a file called `.gitignore` within repository 
2. write name of file to be ignored in  `.gitignore`

## Working with branches 
### Creating Branches
In reality, when working on big projects one does not work in the main branch "master". When many people are working on the project it is useful to create branches. To do it: 
* First choose commit from which you would like to branch with command `git checkout`. _You can choose last worked(head) commit or any other commit_
* Then to create new branch use: `git branch branch_name`

### Navigating in Branches
* To see which branches you have use: `git branch`
* To move between branches use: `git checkout branch_name`

### Merging Branches
When you have finished working in one of the branches, you may want to add new information to the main branch. To do this use merging: 
1. First, got to the _master_ branch or other branch **TO which uou want to merge**
2. Use command: 
```
git merge branch_name
```
### Conflicts
_When Merging two branches you can get a **Conflict**_ 
This happends in case when there is _conflicting_ or different inputs in two branches for the same space.
+ You will atomatically get a message by VS on conflict
+ You will get 3 options: 
1. To choose changes from file TO which you are moving
2. To choose changes from file FROM which you are moving
3. To choose changes from BOTH files 
### Deleting branches
When you  are done working with the branch and have succesfully merged it with the master branch you can delete it, to do it: 
``` 
git branch -d branch_name
```
Some times you can get message: _that the branch is not fully merged and can't be deleted_ 

To delete it anyway use: 
~~~
git branch -D branch_name
~~~

## Working with remote repositiories: 
_GitHub - is a service that allows to integrate different local and remote repositories_
### Getting external repository to your local

### Create remote repository

### Push and Pull

### What is **Pull Request** ? And how to do it? 