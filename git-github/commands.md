# GIT & GITHUB

## Centralized VCS (like SVN) required all the PCs to be connected via network. This was an initial concept of version control. If the central repo crashed, the whole code would be lost.
## Git is a DVCS (distributed version control system).
Subversioning (SVn) was a CVCS (centralized version control system).
DVCS became popular in 2005.
 Git makes it easier to keep track of your code changes using snapshots (saved states).
 Git links the developers to collaborate from remote places and con0tribute in code. It makes work from home possible.
Git provided more reliability, as each workstation had the local repo where the code was stored. In case the central repo crashes, local code is safe.
Why git? It’s free, very compatible with Linux, it was from the Linux foundation.
Can be installed using yum install git.
Benefits of VCS:
Storing versions of code.
Restoring previous version.
Logs make it easy to find bugs.
Backup.
Git Configurations:
To put it simply, git configurations help to identify who has created the commit.
git config –global user.name “rashidwassan”
git config –global user.email “rashidwassaan@gmail.com”
To print the configurations: use git config –list

Git Workflow (creating local repo):


### There are three divisions in Git. 
  - 1: Workspace (code); 
  - 2: Staging Area (where files are freezed, decision making area); 
  - 3: Local repo (where commits are stored).

``` bash
Create a directory (mkdir command).
Initialize git (run git init command in directory), this will create a local repo in that directory (.git directory will be created).
cat>file.txt just to create a file to be tracked. You can make code changes here.
git add . is the command which adds the files staging area. Here ‘.’ is used to indicate all the contents of the directory.
git commit -m “my first commit” moves the contents of the staging area to the local repository. The commit is saved locally with a SHA hash as ID.
git remote add origin “url” connects local repo with central one.
git pull origin master is optional, but if the changes are made to the central repo, this will update the local one with those changes.
git push origin pushes your local code to the central repo (usually hosted on GitHub or GitLab).
This was a typical workflow of Git.
```