# Git commands

## Basic
`git init` Creates a new Git repository

`git status` Inspects the contents of the working directory and staging area

`git add <filename>` Adds files from the working directory to the staging area (it's possible to add multiple files with a single command by writing next filenames separated with a space)

`git diff` Shows the difference between the working directory and the staging area

`git commit` Permanently stores file changes from the staging area in the repository

`git log` Shows a list of all previous commits

## Backtrack
`git show HEAD` Shows the most recently made commit

`git checkout HEAD <filename>` Discards changes in the working directory

`git reset HEAD <filename>` Unstages file changes in the staging area

`git reset <commit_SHA>` Resets to a previous commit in your commit history

## Branching
`git branch` Lists all a Git project's branches

`git branch <branch_name>` Creates a new branch

`git checkout <branch_name>` Used to switch from one branch to another

`merge <branch_name>` Used to join file changes from one branch to another

`git branch -d <branch_name>` Deletes the branch specified

## Collaborating
`git clone <remote_location> <clone_name>` Creates a local copy of a remote

`git remote -v` Lists a Git project's remotes

`git fetch` Fetches work from the remote into the local copy

`git merge origin/master` Merges origin/master into your local branch

`git push origin <branch_name>` Pushes a local branch to the origin remote (or just `git push` if you have enabled setting to push only the branch you are currently on)
