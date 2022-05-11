# GIT & GITHUB

## Centralized VCS (like SVN) required all the PCs to be connected via network. This was an initial concept of version control. If the central repo crashed, the whole code would be lost.
## Git is a DVCS (distributed version control system).
- Subversioning (SVn) was a CVCS (centralized version control system).
- DVCS became popular in 2005.
- Git makes it easier to keep track of your code changes using snapshots (saved states).
- Git links the developers to collaborate from remote places and con0tribute in code. It makes work from home possible.
- Git provided more reliability, as each workstation had the local repo where the code was stored. In case the central repo crashes, local code is safe.
- Why git? It’s free, very compatible with Linux, it was from the Linux foundation.
- Can be installed using yum install git.

### Benefits of VCS:
- Storing versions of code.
- Restoring previous version.
- Logs make it easy to find bugs.
- Backup.

### Git Configurations:
- To put it simply, git configurations help to identify who has created the commit.
```
git config –global user.name “rashidwassan”
git config –global user.email “rashidwassaan@gmail.com”
```
- To print the configurations: use git config –list

Git Workflow (creating local repo):


### There are three divisions in Git. 
  - 1: Workspace (code); 
  - 2: Staging Area (where files are freezed, decision making area); 
  - 3: Local repo (where commits are stored).

## Basic git flow
``` bash
- Create a directory (mkdir command).
- Initialize git (run git init command in directory), this will create a local repo in that directory (.git directory will be created).
- cat>file.txt just to create a file to be tracked. You can make code changes here.
- git add . is the command which adds the files staging area. Here ‘.’ is used to indicate all the contents of the directory.
- git commit -m “my first commit” moves the contents of the staging area to the local repository. The commit is saved locally with a SHA hash as ID.
- git remote add origin “url” connects local repo with central one.
- git pull origin master is optional, but if the changes are made to the central repo, this will update the local one with those changes.
- git push origin pushes your local code to the central repo (usually hosted on GitHub or GitLab).
```
This was a typical workflow of Git.

## Branching in git:
- Branches are created for parallel processing. Allows multiple developers to work on multiple different features while keeping the main branch clean.
- Changes in the staging area are global for every branch (accessible to every bw#
wranch). If a commit is made, those changes will be private to the branch in which it was committed. You can create an infinite number of branches. Branches of one repo can be merged only.
- git branch newbranch will create a branch called newbranch.
- git checkout newbranch will switch current branch with newbranch.
- git merge newbranch will merge this new branch into main/master branch.

### Merge Conflicts
- Merge Conflicts happen when two different branches having at least a single file which has different content in both branches are merged. Git cannot figure out what change to go with. 

## Some extra git commands:
### git status
Displays either your working tree is clean, or there are changes to commit (in that branch).
### git rm –cache file2
This will unstage file2.

### git show <commit id>
Display all the info about the commit.

### git log
Displays the commit id.

## git stash
When you want to record the current state of the working directory and the index, but want to go back to a clean working directory. The command saves your local modifications away and reverts the working directory to match the HEAD commit.
git stash will move your recent, non committed changes to a temporary memory, so that the working tree should be clean to work on a quick fix.

### git stash list
Displays the stash list in indices form.

### git stash apply
Will bring back your changes from temporary memory.

### git stash clear
Clears the stashed items.

### git reset
- git reset filename, has two variants, soft one for simply unstaging files.
- git reset –hard used to delete recent changes.
