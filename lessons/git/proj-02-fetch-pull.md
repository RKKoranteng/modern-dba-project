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

## Make sure local repo is up to date
It is common for your local repo (on your laptop) to fall behind the remote repo. This happens because multiple people are pushing changes (commits) to the remote repo.

Doing a `git push` from your local to remote repo in such an instance is obviously not going to work because of the inconsistencies between the branch. So how do we resolve the possibility of such an issue and ensure we're always working with the most current copy of the remote code base. Simple, fetch and pull the changes from remote to your local repo.

I typically do a `git pull` before starting work in any repo; this will grab the latest changes into my local branch. Let's give it a shot.
```
$git pull
```




