# This file is to assist you with Git demos
## The commands listed below can be used when you are on the respective slide.

## GIT LOG
git log --oneline

git log --pretty='%Cred%h%Creset | %C(yellow)%d%Creset %s %Cgreen(%cr)%Creset %C(cyan)[%an]%Creset’ 

git log --graph --oneline --decorate

git log -p -M --follow --stat -- path/to/your/file

git log -L 15,23:filename.txt

git shortlog


## GIT REFLOG
git reflog


## WHAT FILES HAVE CHANGED
git diff --name-only HEAD~4 HEAD

git log --name-status --oneline [SHA1..SHA2]

git diff --name-only HEAD...master

## I NEED TO SEE WHAT FILES ARE IN A COMMIT
git log show --pretty="" --name-only 0bd7fe63


## BLAME
git blame -L10,+1 fe25b6d^ -- Program.cs

git blame master -- Program.cs

Git Gui blame Program.cs


## HELP I AM IN TROUBLE
Git checkout filename

Git reset --soft –hard <commit>..<commit>

Git reset b81f11f79

Git reset HEAD~3

Git reset filename


## TIME MACHINE
get reflog

git reset HEAD@{index}


## CHANGE COMMIT MESSAGE
git commit --amend


## I FORGOT TO MAKE A CHANGE
git add .

git commit --amend –m “message” 


## I NEED TO MAKE A CHANGE I COMMITTED A FEW COMMITS EARLIER
git rebase –interactive


## I COMMITTED TO MASTER BUT SHOULD HAVE BEEN FEATURE1
git branch Feature1

git reset HEAD~ --hard

git checkout Feature1


## I COMMITTED TO THE WRONG BRANCH
git reset HEAD~ --soft

git stash

git checkout correctBranchName

git stash pop

git add .

git commit -m ”I committed to the wrong branch :-)"


## GIT DEBUGGING
Set GIT_TRACE=true

Set GIT_TRACE_PACKET=true

Set GIT_TRACE_PERFORMANCE=true

Set GIT_TRACE_SETUP=true


### RESET TO FALSE WHEN YOU ARE DONE
Set GIT_TRACE=false

Set GIT_TRACE_PACKET=false

Set GIT_TRACE_PERFORMANCE=false

Set GIT_TRACE_SETUP=false
