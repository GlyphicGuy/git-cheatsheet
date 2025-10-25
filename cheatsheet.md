# Git Cheat Sheet

## Installation
<a href="https://git-scm.com/" target="_blank">Download Git here</a>



**Check version after installation**
```
git --version
```

## Setup 

**Configure your global username**
```bash
git config --global user.name "yourname"
```
**Configure your global email**

```bash
git config --global user.email "youremail@example.com"
```

**Some necessary configs**

```bash
git config --global core.autocrlf "input"
```
```bash
git config --global core.editor "code --wait"
```

**To edit any global configurations**

```bash
git config --global -e"
```

## Basic Commands

**Initialize repository**
```bash
git init
```
**Staging files/changes**
```bash
git add .
```
**Commit the changes locally**
```bash
git commit -m "Your commit message"
```
**Check the repo status**
```bash
git status
```
**Check commit history**
```bash
git log --oneline
```
**To just peak(or checkout) a specific commit point** 
```bash
git checkout <commit-hash>
```

## Resetting the commit(rewrites history)
```bash
git reset <--soft> <--mixed> <--hard> <commit-hash>
```
*Flags usage:*
- **--soft** : to undo the commit but keep changes staged,usually done to make changes to the commit(save point).

- **--mixed** : *[default if not specified]* unstages all the changes after the specified commit, all changes are safe, but are in Modified (or unstaged) state. 

- **--hard** : *[CAUTION!]* Deletes the commit and all the changes that we made after the specified commit.

- commit-hash : hash of the commit to rest to. 

## Reverting Commits(preserves history)

Revert creates a new commit undoing the changes made in the specified commit hash.
```bash
git revert <commit hash>
```

## Staging/Unstaging
**Staging**
```bash
git add <file-names-space-seperated>
```
OR <br> For staging all (MOST USED)
```bash
git add .
```

**Staged to unstaged (tracked)**
```bash
git restore --staged <file>
```

**Staged to Untracked (stop tracking and remove from staging area)**
```bash
git rm --cached <file>
```

## Branching
**Seeing what branch you're on and all the other branches**
```bash
git branch
```

**Creating branches**
*Recommended*
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

**Swithcing branches**

```bash
git switch branch-name
```
OR
```bash
git checkout branch-name
```

## Deleting branches

**Deleting a merged local branch**
```bash
git branch -d branch-name
```

**Deleting an unmerged local branch (forcefully)**
```bash
git branch -D branch-name
```

**Deleting the branch pushed on remote**
```bash
git push origin --delete branch-name
```

## Merging
switch to main or master first,then:
```bash
git merge branch-name
```

## Handling Merge COnflicts

**Accept Incoming / Current change and then the commands below:**

```bash
git add .
git commit -m "resolve merge conflicts"
```

## Stashing

**Do this if you have uncommited changes and want to switch branches**
```bash
git stash
```

**On returning to the stashed changes branch, run the below command to get back the stashed changes on the branch**
```bash
git stash apply
```

**To clear the stash memory later**
```bash
git stash clear
```

# Remotes

**To see all remotes**
```bash
git remote -v
```
- **-v** : stands for verbose(elaborated info)

**To add a remote**
```bash
git remote add origin <https://link-of-the-github-repo>
```
> **origin** : is the name of the remote branch on github, can be anything but conventionally "origin" [Recommended]


**Deleting a remote**

```bash
git remote rm <remote-name>
```

## Pushing code to Remote
```bash
git push -u origin <branch-name>
```
Flags:
- **origin** : name of the remote
- **-u** : upstream
- **branch-name** : this is probably going to be your "main" or the feature branches you create

## Pulling from Remote

### Fetch & Merge Approach

1. First fetch from remote
```bash
git fetch origin
```
2. The changes will be fetched as a branch called "origin/main" (if named conventionally as followed above)

3. **Check if you are on the main branch** and then run the below command
```bash
git merge origin/main
```
### Pull Approach (Easier)
This is a single command as a combination of Fetch and Merge commands.
```bash
git pull origin main
```

- **origin** : name of the remote
- **main** : name of the main branch
<br>
<br>
<br>
# Visualizing git - Tool for practice and understanding
### https://git-school.github.io/visualizing-git/#free