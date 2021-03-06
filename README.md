# demo-repo
name: kevin wong\
file: readme.md\
date: 12/26/21\
desc: learning git from ![freeCodeCamp](https://www.youtube.com/watch?v=RGOj5yH7evk&t=192s)

demo repo to learn git

## What is version control
The management of changes to document, computer programs, large websites, and other collections of information
Good for tracking and looking at previous instances.




## Terms
* directory => folder
* terminal or Command line => Interface for text commands
* CLI => command line interface
* cd => change directory
* code Editor => Word Processor for writing code
* repository => Project, or the folder/place where your project is kept

## Git commands
* clone => bring a repo that is hosted remotely into a folder on your local pc
* add => track your files and changes in git
   * git add . tracks all files that have been changed
   * or
   * git add \<filename\> to track that specific file or folder
* git status => list status of tracked and untracked files
* commit => save your files in git
   * changes are made to the .git foler locally
* push => upload git commits to a remote repository, like github, bitbucket....etc
   * git push origin master => "origin" is an option for location of git repository and "master" is the name of the branch
* pull => down changes from remote repo to your local machine, the opposite of push

## Branches
* git branch => shows what branch you are in (master is normally the parent branch)
* git checkout -b \<branch name\> => creates a branch
* git add \<filename\> => stage or track the files that have been modified
* git commit -m "describe what was done"
* git diff \<branch name\> => shows what lines of code(from "branch name") was changed compared to the "master" branch
* git merge \<branch name\> => will merge lines of code(from "branch name") to "master branch"
   * note: more commonly we see the branch pushed into github then making a pull request (pr)
   * so let's do the more common method
   * git push => this will prompt you to set the the upstream for the new branch using the command provided to you.
* once your branch is merged, you will often delete your source branch and switch back to the master branch
* if you want to create a new pull request (pr), you will do it from a new branch and start the process over again
* git checkout \<master\> => switch back to master locally. GETs most recent master branch to local pc
* git pull => to get the most recent master branch
* git branch -d \<name of branch you want to delete\> => almost never reuse branches that have been merged, so delete them
* pull master to local repo because other people are also merging into master as well and you should have the most up to date code when working on features

## Undoing a commit
* git reset \<filename\> => reverts last commit to file
* git reset head~1 => also works if you don't have the filename
* don't forget to use "git diff" to compare changes
* git log => to see a log of the commits.
   * you can use the unique commit hash in git reset --hard \<hash number\> to undo all the subsequent commits including the one referenced with hash number

## Forking
* you fork because you might not have full administrative permissions to the repository and/or the files
* once forked into your repository you have full permission to edit the full repository
* If you wanted to get your changes into the original repository you would make a pull request (pr)


------------------------------------------------------------------------------------------------------------------------------------------------------------

note: md = markdown text

note: the ".git" hidden folder contains all commits and code changes over time from the beginning of repository. Use "ls -a" command in bash to view hidden folders.

note: when you modify code in VS Code a "M" appears next to the file in the "explorer" tab

note: git commit -am OR git commit -a -m => adds and commits at the same time
   * this only works for modified files!!! example: modified: index.html
   * this won't work for created files, example: created: index.html
      * you would follow the staging process, git status, git add \<filename\>, git commit -m "description"
 
