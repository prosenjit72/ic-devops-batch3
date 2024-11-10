                            Git - A Version Control System

To walkthrough git commands we first need to know what git is. The purpose of git, and how to use it.
In simple terms, Git is a version control system tool. It helps to keep track of changes in our files when we are are collaborating with many people. We can save different versions so that we may revert to them if need be.
The Purpose of Git shows the power it holds. Its purpose are:

1.  **Version Control**: Git helps us to keep track of changes in our files over time. We can see when what was changed and by whom.
2.  **Collaboration**: Multiple people, even multiple teams can work together whilst maintaining each of their work. Git helps everyone work together without overwriting or deleting any one's work.
3.  **Backup**: Git keeps track of everything in it's .git file. All the work history with timestamp and user trails is stored. IF anything goes wrong, git helps it's user to revert to an earlier uncorrupted version of their work.
4.  **Branching**: For a major Big Project it is utmost necessary to keep track of work and also ensure every collaborator can fluidly without interruption continue their work. Git Branches help do just that. We can create branches to work on some new features or bugs without affecting anyone else. Once we are happy with our changes we can incorporate our work with the main project through Merging.

We have talked about git and it's purpose. Now, how does this actually function as each people have their own machine (i.e PC). Introduce **Git repository** or repo.
It is a storage space where all the files of a Project and the history of changes made to those files are kept. This is the main benefit of Git. We can store files and work on them sitting anywhere in the world whilst maintaining each of our work. It is the heart of a Git project. A Repo is two types, 1. Local Repo and 2. Remote Repo.

A Local Repo: is on our own machine, we can work independently through it.
A Remote Repo: is hosted on a server e.g GitHub, GitLab, GitBucket etc. It is used for collaboration.

A Git repository is where the project lives. We can create local repositories for personal work and use remote repositories for teamwork.

Let's jump into git commands now. The How to Use Git.
There are many git commands. These commands are what make Git work. They are:

1. Initialize a Repo -- git innit : This command creates a new Git Repository in the project folder.

2. Check the Status -- git status : It shows the current status of our files (Changed, Staged or Untracked)
   ![git status](./screenshots/git%20status.PNG)

3. Add Changes -- git add <file> : This command can stage a single file or even all files in the repository.
   ![git add command](./screenshots/git%20add.PNG)

4. Commit Changes -- git commit -m "Message" "Description(Optional)": This saves our staged changes with a message.
   ![git commit command](./screenshots/git%20commit.PNG)

5. Commit Edits -- git commit --ammend : This command allows us to modify the most recent commit. We can change the commit message or add new changes to the last commit. It’s useful
   for correcting mistakes or adding forgotten files.
   ![git commit --amend command](./screenshots/git%20commit%20--amend.PNG)

6. Reseting Commit -- 3 types:- Soft Reset, Hard Reset and Mixed Reset; Mixed Reset is the default beahior. :
   a) Soft Reset: Moves the HEAD pointer to a previous commit but leaves your working directory and staging area unchanged. This allows you to re-commit changes.
   ![git soft reset command](./screenshots/git_soft_reset.PNG)

   b) Mixed Reset: This is the default behavior. It moves the HEAD pointer to a previous commit and resets the staging area, but leaves the working directory unchanged.

   c) Hard Reset: Moves the HEAD pointer to a previous commit and resets both the staging area and working directory. This command will discard all changes made after the specified commit.
   ![git reset --hard command](./screenshots/git%20reset%20--hard.PNG)

7. View all branches -- git branch : This command shows all branches created.
   ![git view branches command](./screenshots/git%20checkout_branch.PNG)

8. Merge Branches -- git merge <branchname> : This command integrates changes from the specified branch into the current branch. It combines the commit histories of both branches. If there are conflicts, Git will prompt the merger to resolve them before completing the merge.
   ![git merge command](./screenshots/git%20merge.PNG)

9. View reflog -- git reflog : This command shows a log of all the actions (like commits, checkouts, merges) that have affected the current branch. It’s useful for recovering lost commits or
   understanding the history of our branch.
   ![git view reflog command](./screenshots/git%20reflog.PNG)

10. Push Changes -- git push : This command uploads your local commits to a remote repository. It updates the remote branch with our changes, making them available to others. The remote
    name is mentioned, like: git push origin, here origin is the remote. And then add the branch name after the remote name. So, the final command is something like: git push origin main.

11. Pull Changes -- git pull : This command fetches changes from a remote repository and merges them into your current branch. This command is a combination of "git fetch" and "git
    merge" commands. It is similar to git push. The final command is something like: git pull origin main.

12. View History -- git log : This command shows the history of all commands with the messages and their timestamps.
    ![git log command](./screenshots/git%20log.PNG)

13. Create and Switch to new branch -- git checkout -b <branchname> : This command creates a new branch with the specified name and immediately switches to that branch. It is a
    convenient way to start working on a new feature or fix without affecting the main branch.
    ![git checkout and switch to branch command](./screenshots/git%20branch.PNG)

14. Clone a Repository -- git clone <repository-url> : This command creates a local copy of a remote repository. It downloads all the files, commit history, and branches from the
    specified repository URL to our local machine.

15. Delte remote branch -- : This command is used to delete a branch from a remote repository. It tells Git to push a deletion request for the specified branch to the remote repository.
    After executing this command, the branch will no longer exist on the remote server.
    ![git delete remote branch command](./screenshots/git%20delete%20remote%20branch.PNG)

16. Delete local branch -- : The command of deleting branch locally can be divided into two. Based on their status on being merged, the command changes.
    git branch -d branch_name
    This command is used to delete a local branch from your repository. The -d option stands for "delete" and will only allow the deletion if the branch has been fully merged into the current branch. If the branch has unmerged changes, Git will prevent the deletion to avoid losing work.

    git branch -D branch_name
    If we want to forcefully delete a local branch regardless of its merge status, we can use the -D option.
    ![git delete local branch forcefully command](./screenshots/git%20delete%20local%20branch.PNG)

17. Create a remote -- : This command is used to add a new remote repository to our local Git configuration. A remote is a version of our project that is hosted on the internet or
    another network. By adding a remote, we can easily push and pull changes to and from that repository.
    ![git add remote command](./screenshots/git%20add_remote.PNG)

18. Show all remotes -- git remote -v : This command lists all the remote repositories associated with our local Git repository, along with their URLs. The -v option stands for
    "verbose" and shows both the fetch and push URLs for each remote.
    ![git view remotes command](./screenshots/git%20remotes.PNG)

19. git restore : This command is used to restore files in our working directory to their state in the last commit or a specified commit. It's useful when we want to discard changes made to a file since the last commit,
    effectively reverting it back to its last committed state.
    ![git restore command](./screenshots/git%20restore.PNG)

20. git restore --staged : This command is used to unstage a file that has been added to the staging area (index) without affecting the working directory. This means that the changes in the file will remain intact, but
    the file will be removed from the staging area, making it ready to be committed.
    ![git restore --staged command](./screenshots/git%20restore%20--staged.PNG)

21. Applying git commit of one branch to another -- git rebase <target_branch>: This command takes the commits from the current branch and replays them on top of the specified target
    branch. It’s useful for integrating changes while maintaining a linear commit history.

22. PR checkout -- git pr checkout {#number} : This command is used in some Git hosting services (like GitHub) to check out a pull request by its number. It creates a new branch based
    on the pull request, allowing us to review or test the changes.
