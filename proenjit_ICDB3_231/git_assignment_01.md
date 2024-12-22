## Basic git commands
Followings are the basic commands of git
## How can I clone a remote Git repository?
git clone <remote-repository>

## git add-"Used to add changes in your working directory to the staging area in Git"
git add .
or 
git add <file-name>

## git commit-"Used to save your staged changes to the local repository in Git"
git commit -m "<Your commit message>"

## Create and switch to the new branch
git checkout -b <branch-name>

## Purpose of git Branch?
 Git branches help the development workflow, allowing you to manage multiple development lines, safely experiment, and collaborate efficiently.

## What is git alias?
 Git alias is a shortcut or custom command that allows you to define a simpler or shorter version of a longer or more complex Git command.
## alias cmd-
 git config --global alias.<alias-name> '<git-command>'
# Here --global means the alias is available across all Git repositories for your user account

## What is git reset?
Git reset is a command that reverts changes to your Git repository and returns the working environment to a previous state. Hard reset, Soft reset, Mixed reset, There are three types of git reset. 

## Soft Reset
## If I perform a soft reset, it will undo the last commit, and will remain in the staging area.
git reset --soft <commit>

## Mixed Reset
If I perform a Mixed reset, it will undo the last commit, and will remain in the unstaging area.
## Syntax
git reset --mixed <commit>

## Hard Reset
If you perform a hard reset, it will delete the commit and also remove the files from the working directory.
## Syntax
git reset --hard <commit>

## Purpose of git reset!
 Remove a wrong commit, Clear the staging area, Delete all changes (both staged and unstaged) and return to a clean state.
