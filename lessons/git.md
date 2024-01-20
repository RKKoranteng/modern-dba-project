# Git
* [What is Git](#what-is-git)
* [Git vs GitHub vs GitLab](#git-vs-github-gitlab)
* [Basic Git terminology](#basic-git-terminology)
* [Git states](#git-states)
* [Practice](#practice-1)

## What is Git?
Git is an open-source command line Version Control System (VCS) originally developed in 2005 by Linus Torvalds (the guy who created Linux os/kernel). There're a few VCS's in the market, but Git has become the clear leader because it's the engine behind many popular source control tools such as Github, Gitlab, Bitbucket. Also, the Git engine works well on a wide range of operating systems and IDEs (Integrated Development Environments). Git helps teams work faster and smarter; it's especially useful for DevOps teams since it helps to reduce development time and increase successful deployments.

Git (also known as source control) is used to track and manage changes to code. Like other version control software, Git keeps track of every modification to code. If a mistake is made, you can turn back the clock and compare earlier versions of the code to help fix the mistake while minimizing disruption to all team members. Git does alot, but here're a few important things to know about Git:

* Git keeps track of every modification to source code
* Git support ability to rollback to previous versions of source code
* Git allows multiple developers to work collaboratively

## Git vs GitHub vs GitLab
You've probably heard of Github or GitLab, and you may even wonder how are they different from Git. Simply put, Git is the engine behind GitHub and GitLab. Both GitHub and GitHub are web-based VCS that've put nice UI ontop the native Git engine. If you want, you can use GitHub or GitLab from the user friendly website (no git commands needed), however if you are a geek like me then you'd prefer the git command line. Git commands are the same regardless if you are using GitHub, GitLab, Bitbucket, or any other VCS running on git. The only thing that is different is the UI, a few terminilogies and functionalities. For example GitHub's CI/CD deature is called 'GitHub Action' where as GitLab's CI/CD is called "GitLab CI'. My advice to you is to learn git commands because their transferrable accros any git-powered VCS.

## Basic Git terminology
Let's get familiar with some common git terms.

* **Repository (repo)**: A Git repository acts as a directory that stores all the content (code, files, images, etc) needed for your project.
* **Init**: `git init` command is used to start tracking a directory, which means it's now a git repo.
* **Clone**: `git clone` command is used to a copy of a repo.
* **Branch**: A branch is a version of the repo.
* **Checkout**: `git checkout` command is used switch between branches in a repo.
* **Commit**: `git commit` creates a saves modifications made to repo. It essentially crrates a savepoint/napshot of the repo.
* **Local repo**: Local repos reside on the computers of team members.
* **Remote repo**: Remote repos are hosted on a server accessible for all team members (most likely on the internet or local network).
* **Push**: `git push` command updates a remote repo with the commits made to the locl repo.
* **Status**: `git status` command shows the working tree status; what files have been modifed, marked to be saved, and which files aren't being tracked in repo. 

## Git states
Git has three main states that your files can reside in; modified, staged, and committed.

* **Modified**: means that you've made changes to your file but have'nt staged it yet. The modified file is logical place in 'Working Directory'.
* **Staged**: means that you have marked a modified file to be added to your next commit. Staged files are logically placed in 'Staging Area'.
* **Committed**: means that staged file has been successfully saved to git database. Committed files are logicallt placed in 'Git Directory'.

<p align="center"><img src="../images/git-areas.png" ></p>

## Practice 1
```
# create a unversioned/untracked directory
$ mkdir my-interests

# turn directory into a git repo
$ cd my-interests
$ git init

# create a untracked file in repo
$ echo "Meditations (by Marcus Aurelius)" > fav-books.txt

# see working tree (repo status)
$ git status

# add modified file to git staging area
$ git add fav-books.txt

# see working tree to see change after staging file
$ git status


# save modified file into git directory
$ git commit -m 'adding my favorit books'
```
