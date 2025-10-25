# Git Cheat Sheet

## Installation
[Download Git here](https://git-scm.com/)

check version 
```
git --version
```

## Setup 

```bash
git config --global user.name "yourname"
```
```bash
git config --global user.email "youremail@example.com"
```
```bash
git config --global core.autocrlf "input"
```
```bash
git config --global core.editor "code --wait"
```
for editing:
```bash
git config --global -e"
```

## Basic Commands

```bash
git init
```

```bash
git add .
```

```bash
git status
```

```bash
git log --oneline
```

```bash
git commit -m "Your commit message"
```

```bash
git reset <--soft> <--mixed> <--hard> HEAD~<n commit back>
```

revert creates a new commit undoing the changes made in the specified commit hash 
```bash
git revert <commit hash>
```

to just peak at a specific commit point 
```bash
git checkout <commit hash>
```

staged to unstaged (tracked)
```bash
git restore --staged <file>
```

staged to untracked (stop tracking and rm from staging area)
```bash
git rm --cached <file>
```

## Branching
seeing what branch you're on and all the other branches
```bash
git branch
```

creating branches 
```bash
git checkout -b branch-name
```
OR
```bash
git switch -C branch-name
```
OR
```bash
git branch branch-name
```

swithcing branches
- 
```bash
git switch branch-name
```
OR
```bash
git checkout branch-name
```

deleting branches
-
deleting a merged local branch
```bash
git branch -d branch-name
```

deleting an unmerged local branch (forcefully)
```bash
git branch -D branch-name
```

deleting the branch pushed on remote
```bash
git push origin --delete branch-name
```

## Merging
switch to main or master first,then:
```bash
git merge branch-name
```

## Handling Merge COnflicts

Accept Incoming / Current change

```bash
git add .
git commit -m "resolve merge conflicts"
```

# Stashing

do this if you have uncommited changes and want to switch branches
```bash
git stash
```

On returning to the stashed changes branch, run the below command to get back the stashed changes on the branch
```bash
git stash apply
```

To clear the stash memory later
```bash
git stash clear
```







```bash
git push origin main
```



## visualizing git tool for practice and understanding
### https://git-school.github.io/visualizing-git/#free