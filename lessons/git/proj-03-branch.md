# Doing a fetch and pull
This practice will:
* get you hands-on experience creating git branch
* understand how to navigate between branches
* teach you how to list all bracnhes in a repo

**Tools needed**
* [GitHub](https://github.com/join)
* [Git Bash](https://git-scm.com/downloads)
> Launch Git Bash application to run all Git commands

<p align="center"><img src="../../images/git-pull-vs-fetch.gif"><br/><small><i>image: https://www.theserverside.com</i></small></p>

## Why keep local and remote branches in synch?

Let's get hands-on with branches.
```
# this command shows all branches created for a local repo
# note, this example output shows that there's only one branch (default main branch)
# also note the '*' next to the 'main' branch signifying this is the current branch (the branch you're currently in)
$ git branch --list
* main

# there're multiple ways to create a new branch. See below:
#  -> way 1: 'git branch test' will create a new branch called test
#  -> way 2: 'git checkout -b test' will create a new branch called test, then it will switch into it (making it the current branch)
# in the example below, you'll create a new branch called 'add-genre' and switch into it
$ git checkout -b 'add-genre'

# list all branches in this repo and see which is the current branch
# you should see the new branch (add-genre) is the current branch
$ git branch --list
```
