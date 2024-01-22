# Doing a fetch and pull
This practice will:
* get you hands-on using git fetch and pull
* understand when to use git fetch and pull
* troubleshoot when remote repo is ahead of local repo

**Tools needed**
* [GitHub](https://github.com/join)
* [Git Bash](https://git-scm.com/downloads)
> Launch Git Bash application to run all Git commands

<p align="center"><img src="../../images/git-pull-vs-fetch.gif"><br/><small><i>image: https://www.theserverside.com</i></small></p>

## Why keep local and remote branches in synch?
It is common for your local repo (on your laptop) to fall behind the remote repo. This happens because multiple people are pushing changes (commits) to the remote repo.

Doing a `git push` from your local to remote branch in such an instance is obviously not going to work because of the inconsistencies between the branches. You'll get a nice error like this:
```
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
The error is self-explanatory. So how do we resolve the possibility of such an issue in the first place; simple, ensure you're always working with the most current copy of the remote code base. 

I typically do a `git pull` before starting work in any repo; this will grab the latest changes into my local branch. Let's give it a shot.

## 1. Check to make sure local and remote branches are in synch
In this example, you're going to ensure both your local and remote branches are in synch
```
# use git fetch command to compare local and remote branches
# if the command does not return anything, it means your local and remote branch are in synch
# else if the command returns a message saying something about 'Enumerating objects ..', then you know there're inconsistencies between the local and remote branch
$ git fetch

# no need to run git status if your branches are in sync
# but if you want you can still check the working tree of your local branch
# you should get a message saying that 'Your branch is up to date ...'
$ git status
```

## 2. Force your remote branch to be ahead
When your remote branch is ahead of your local that means that there's been commit(s) pushed to your remote branch that have not been applied to your local branch. Let's force the remote branch to be ahead.
* Navigate to your remote repo in GitHub
* Edit 'README.md' by adding a new entry ... put whatever you want
* Save and commit directly to you branch

Your remote branch is ahead of local branch now because this most recent commit exists in the remote, but not in the local.

## 3. Grab remote changes
Now that we've forced inconsisties between the local and remote branches, let's see how to re-sync the branches
```
# first use git fetch to compare the local and remote branch
# you should get an message that says something 'Enumerating objects ...' 
$ git fetch

# if you want more details you can use git status command to see exactly the differences captured during the comparison
# You should get a message saying something about 'your local branch is behind ...'
$ git status

# use the git pull command to synch your local branch with remote branch (this is also known as fast-forwarding a branch)
$ git pull

```

At this point your local branch has been successfully synched with remote branch. You can view the file ('README.md') to ensure the changes from remote branch (GitHub) has been applied to your local branch (your laptop).




