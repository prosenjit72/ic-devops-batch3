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

## What is Git rebase?
Git rebase is a command used to reorganize the commit history of one or more branches.
## Purpose of git rebase!
Suppose I have 10 commits, and they might be related to different files. Now, I want to edit or update an existing file. For this, at the beginning, I use:
git rebase -i HEAD~7
## Here, 7 refers to the last 7 commits. After running the above command, the commit file will open. Then, I find the commit I want to edit, mark it as edit, and exit by typing wq. Now, the repository enters rebase mode. Then I make the necessary changes to the file and Stage the changes using git add .

## Update the commit with:
git commit --amend

git rebase --continue 
## The command git rebase --continue is used during an ongoing Git rebase process to proceed after resolving any conflicts or making necessary changes.

## What is Git Squash?
In Git, squashing refers to the process of merging multiple commits into a single commit. It is commonly used to keep the commit history clean and organized, especially before merging into the main branch.
## Syntax
git rebase -i HEAD~N