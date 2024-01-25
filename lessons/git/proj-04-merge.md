# Merging branches
This practice will:
* get you hands-on experience creating git branch
* understand how to navigate between branches
* teach you how to list all bracnhes in a repo

**Tools needed**
* [GitHub](https://github.com/join)
* [Git Bash](https://git-scm.com/downloads)
> Launch Git Bash application to run all Git commands

<p align="center"><img src="../../images/git-branch.png"><br/><small><i>image: https://codeinstitute.net</i></small></p>

## Checkout a branch

Checkout the 'navbar' branch
```
# confirm 'navbar' branch exist
$ git branch --list

# switch into 'navbar' branch
$ git checkout navbar
```

## Add changes

Now that you're in the 'navbar' branch, edit README.md to add genre for your favorite books. See example output of my README.md file below.

```
My favorite books

 - Motivational
   1. Meditations (by Marcus Aurelius) 
   2. Atomic Habits (by James Clear)

 - Tech
   1. SRE Hanbook (by Google)
```

## Commit changes
```
# mark the modifications to be added to your next commit`
$ git add README.md

# commit the changes with your desired message (my example is 'adding genre')
$ git commit -m 'adding genre'
```

## Merge into main
```
# swicth to the 'main' branch since this is the branch we want to merge into
$ git checkout main

# merge the 'navbar' branch
$ git merge navbar

# at this point you can push the changes from local repo 'main' branch to your remote repo
# refresh your remote repo UI (GitHub) to see the changes posted
$ git push
```

> If your'e like me and don't like keeping uncessary stuff then you can delete the 'navbar' branch since it's been merged successfully. Here's an example command. `git branch -d navbar`
