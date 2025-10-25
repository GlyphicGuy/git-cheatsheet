# what to expect

- teaching what matters
- rare cases? use gpt and how to
- NOT for open source!

# main content

### Understand the problem:

- collaboration pov
    - send over WA mail etc

- idea of a central code base
    - SSOT single source of truth
    - working offline locally
    - breif idea of code push and retrival etc collaboration stuff

- the idea of VCS or "git"
    - concept of snapshotting state (like a checkpoint or save point)
    - ctrl Z??? for a 100 files?? nope
    - timeline and code management stuff
    
- git on internet is github

![alt text](image.png)

# HANDS ON!

- git installation

- git initial setup

- initialize git repo



stages:
U - untracked
A - added or staged
C - Commited
M - Modified


explaining on the smartboard using excalidraw etc






- managing your own projects
- making git available in our project
- making a checkpoint or saved point
- adding files
- staging them
- commiting them
- going back to some previous saved point
- logging everything
- reverting back to the previous saved point
- peak into the prev commits

commands you need to know -
git status -s => to know current status of unstaged and staged files

# Branching

- different ppl on diff features
    at the same time
- merging issues with multiple ppl trying to merge 

## visualizing branching
### https://git-school.github.io/visualizing-git/#free

- seeing all branches
- branching out
- swithing branches

# merging

- visualize the merging scenario
- conflict scenarios
- resolving that
    - types of merge on conflicts:
        - three way merge - usual merge
        - ff merge - only 1 branch and no update on main

# stashing

- purpose 
- commands

---

# Collaboration Flow!

1. main person inits repo & uploads to github 

2. adding others as collaborators on Github
    
    ---
3. Collaborators clone from the main repo

4. [IMPORTANT!] create their own feature branches and ONLY THEN start to work. Never work or commit to main branch directly unless you know what you're doing

5. commit and push to upstream (github main repo)

6. inform about the commit to the main person
    ---

7. main person checks the commits and merges to main.


# Managing Project Flow!
**When you start a new Project**
1. initialize git repo (git init)
    - main branch is called master, you can change it to main (git branch -M main)
2. make the initial setup as per your project
    - writing boilerplate  code
    - basic folder structure
    - initial code for project's existence
3. stage the changes (git add .)
4. git commit -m "initial commit"
5. make a repo on the GitHub and copy the url
6. add remote (git remote add origin <url>)
7. git push -u origin main
8. refresh the github tab to see the changes uploaded.

---
**steps 9-12 is the repeated workflow usecase**

9. make changes to the project(add/edit/delete files/folders)
10. stage them again (git add .)
11. git commit -m "any message you want"
12. git push origin main (or just git push if pushing to the same branch anyways)
---






