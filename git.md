---
aliases: 
tags:
- public
- knowledge
- tool
date created: "2022-04-13T12:29:53"
date modified: "2022-04-13T12:50:56"
title: Git
---

# Git

## Setting up Git

```zsh
git config --global user.name “Firstname Lastname”
git config --global user.email “[blabla@bla.com](mailto:blabla@bla.com)”
git config --global color.ui true
```

## Start a Repo

```zsh
mkdir store
cd store
git init
```

## Own Repo

`git status` -> check what has changed since the last commit

`git add README.txt` -> add a file to the staging

`git add <list of files>` -> add the list of files

`git add --all` -> add all changed or created files to the staging

`git add *.txt` -> add all text files in the current directory

`git add docs/*.txt` -> add all text files in docs directory

`git add docs/` -> add all files in docs directory

`git add “*.txt”` -> add all text file of the whole project.

`git rm README.txt` -> removes README.txt

`git commit -m “Create a README”`

`git log` -> look at the timeline, listing all commits

`git diff` -> look at differences between the staged project and the unstated project

`git diff --staged` -> look at changes made in the stage

`git reset HEAD README.txt` -> taking a file away of the staging

`git checkout -- README.txt` -> remove all changes since the last commit

`git commit -a -m “Modify readme”` -> add all changed files to stagiing and commit it -> no new files

`git reset --soft HEAD^` -> remove last commit and put it back to the staging

`git reset --hard HEAD ^` -> undo last commit and all changes

`git reset --hard HEAD^^` -> undo last 2 commits and all changes

`git commit --amend -m “Modify readme & add todo.txt.”` -> add the current staging to last commit

## Remote Repo

`git remote add origin https://github.com/Gregg/git-real.git` -> add a remote named “origin”

`git remote rm origin` -> remove the remote “origin”

`git remote -v` -> show remote repositories

`git push -u origin master` -> push the local master branch to the repository origin

password cashing -> [https://help.github.com/articles/set-up-git](https://help.github.com/articles/set-up-git)

`git pull` -> update local Repo

`git clone https://github.com/codeschool/git-real.git` -> clone remote repository to git-real

`git clone https://github.com/codeschool/git-real.git git-demo` -> clone remote repository to git-demo

## Branches

`git branch cat` -> create new branch

`git branch` -> see which branch we’re on

`git checkout cat` -> change branch

`git branch -d cat` -> delete branch

`git checkout -b admin` -> create branch at switch to it

```zsh
git checkout master
git merge cat
```

-> merge cat to master branch

if merge opens up vi:<br>h = left, j = down, k = up, l = right, esc = leave mode, i = insert mode,<br>:wq = save & quit, :q! = cancel & quit

`git commit -a` -> after merge conflict is resolved

`git push origin shopping_cart` -> pushing a branch to remote repo

`git branch -r` -> list all remote branches

`git checkout shopping cart` -> automatically creates local branch and switches to it

`git remote show origin` -> shows all branches (local and remote)

`git push origin :shopping_cart` -> delete repo branch

`git branch -D shopping_cart` -> deletes local branch, ignoring the warnings

`git remote prune origin` -> deletes branches that are not on the remote project anymore

## Tags

`git tag` -> list all tags

`git checkout v0.0.1` -> checks out the code at tag v0.0.1

`git tag -a v0.0.3 -m “version 0.0.3”` -> add new tag

`git push --tags`

## Rebase

```zsh
git fetch
git rebase
git rebase - -continue
git rebase - -skip
git rebase - -abort
```

## Logging

`git config --global color.ui true`

`git log - -pretty=oneline`

`git log --pretty+format: “%h %ad- %s [%an]”`

%ad = author date<br>%an = author name<br>%h = SHA hash<br>%s = subject<br>%d = ref names

`git log --oneline -p` -> shows changes

`git log --oneline --stat` -> shows how many deletions and insertions were made

`git log --oneline --graph` -> shows a visual representatijon of the branch marching into master

```zsh
git log - -until=1.minute.ago
git log - -since=1.day.ago
git log - -since=1.hour.ago
git log - -since=1.month.ago - -until=2.weeks.ago
git log - -since=2000-01-01 - -until=2012-12-21
```

```zsh
git diff HEAD^
git diff HEAD^^
git diff HEAD~5
git diff HEAD^ . . HEAD
git diff 4fb063f . . f5a6ff9 -> range of SHAs
```

`git diff master bird` -> diff between two branches

`git diff --since=1.week.ago --until=1.minute.ago` -> time-based diff

`git blame index.html --date short` -> lists changes of a file

## Configuration

`.git/info/exclude` -> files in here get excluded

`git rm - -cached development.log` -> deleting file from git but not from filesystem

.gitignore -> `logs/*.log`

`git config - -global core.editor emacs` -> use emacs for interactive commands

`git config - -global merge.tool opendiff` -> use opendiff for merging conflicts

`git config user.email “[blabla@bla.com](mailto:blabla@bla.com)”`

```zsh
git config - -global alias.mylog \ “log - -pretty=format: ‘%h %s [%an]’ - -graph”
git config - -global alias.lol \ “log - -graph - -decorate - -pretty=oneline - -abbrev-commit - -all”
```
