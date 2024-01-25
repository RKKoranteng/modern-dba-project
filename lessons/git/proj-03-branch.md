# Working with branches
This practice will:
* get you hands-on experience creating git branch
* understand how to navigate between branches
* teach you how to list all bracnhes in a repo

**Tools needed**
* [GitHub](https://github.com/join)
* [Git Bash](https://git-scm.com/downloads)
> Launch Git Bash application to run all Git commands

<p align="center"><img src="../../images/git-branch.png"><br/><small><i>image: https://codeinstitute.net</i></small></p>

## Display all branches

Let's get hands-on with branches. This command shows all branches created for a repo
```
# note, this example output shows that there's only one branch (default main branch)
# also note the '*' next to the 'main' branch signifying this is the current branch (the branch you're currently in)
#
$ git branch --list
* main
```

## Create a branch

There're multiple ways to create a new branch. See below:
* Approach #1: use `git branch <branch name>` to create a new branch
* Approach #2: use `git checkout -b <branch name>` to create a new branch, then automaically check it out (switch into it); making it the current branch
```
# in the example below, you'll create a new branch called 'add-genre' and switch into it
# to understand the command, we'll read the syntax from right to left
#
#   -> the branch name in this example is 'add-genre'
#   -> the '-b' flag/option signifies we're creating a new branch 
#   -> the 'checkout' command is used to switch to the newly created branch
# 
$ git checkout -b 'add-genre'

# list all branches in this repo and see which is the current branch
# you should see the new branch (add-genre) is the current branch
#
$ git branch --list
```
