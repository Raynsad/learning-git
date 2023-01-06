# What is Git?
The industry standard distributed version control system

## What problem does it solve?
- Alice and Bob are working on a project together for school
- They need to share code and turn it in
- They don't know the proper way to do this, so they paste their code into a Google Doc

### Problem 1:
- Alice and Bob copy the Google Doc into their own IDE's
- They both make changes separately
- Some secret tests are passing in Alice's environment, and others are passing in Bob's environment
- They cannot tell which parts of the code were written by who, nor can they merge the two versions together without a ton of effort

### Problem 2:
- The night before submitting the project, both Alice and Bob make changes to different parts of the code
- They compile the code and the program breaks. They want to go back to an old version to try and fix the breaking changes
- How do they revert JUST the breaking changes?

### Problem 3:
- Alice and Bob finally complete their project
- The night before submission is due, Evil Eve logs onto their Google Doc and makes breaking changes in their code
- Alice and Bob have no way of stopping this from happening, nor do they have any record of what was changed and when

## Enter Git
- Git organizes your code into commits, which are atomic sets of changes to the code.
- A commit contains: file diff, author, timestamp, previous change hash
- Git will store these commits as a log that shows the history of commits
- Git supplies many useful commands to create, edit, roll back, publish, merge, etc.
- We will get into the specifics of how this works when we run through a demo

## What is GitHub?
- GitHub is a version control platform that provides Git services
- Git is the tool, GitHub is the network that hosts code and facilitates the use of git
- Both Git and GitHub are the most common industry standard

## What does GitHub do?
- A social network for git users
- A place to keep a copy of the repository
- A means to exchange and validate changes between people on a team
- A database of change requests, comments, and approvals
- Other cool stuff outside the scope of this demo

# Demo time

## Clone a repository
### What is a repository?
- The place where the code lives
- Contains source code
- Contains all the history information
- Contains all the branches
- Contains git-specific files (.git, .gitignore, ...)
### Cloning the remote:
In our case, the remote repository lives in GitHub.

Navigate to this repository in GitHub Desktop.
- Choose a file path where you want this repository to be saved in your local file system
- This file path will contain your local copy of the repository
- Your local repository is set up to push and pull changes from the remote

## Fetch code from the remote
Fetching updates your local repository with all the latest history from the remote.
- Navigate to "fetch" in GitHub Desktop
- It may then prompt you to "pull" the code into your local branch. This updates the code on that branch

## Create a branch
### What is a branch?
- A version of the source code within the repository
- Each branch contains its own history of commits
- Typically, a branch is used for individual development and then merged into a main branch
- When you create a branch for the purpose of making a change, adding a feature, or fixing an issue, it is called a feature branch

### Creating the branch:
It is standard practice to create a branch any time you are working on a shared repository. Do not push changes directly to `develop`, `main`, etc. 

Navigate to "current branch" in GitHub desktop and select "new branch."
- Notice the pop-up specifying which branch this new branch will be based off of; your new branch will start out as a copy
- This branch now exists in your local repository, but not the remote

## Write some code
Open any text editor and edit a file in the repository
- Some IDE's and text editors have built-in git functionality or plugins, such as Visual Studio Code
- These are optional; as long as you save the changes from any editor, git will track them

## Stage  your changes
### What is staging?
- Simply saving changes to a file does not automatically add them to git's history
- Notice how GitHub Desktop displays changes in its UI once you save the file
- These are the staged changes, AKA the changes that will make it into your next commit
GitHub Desktop handles staging mostly automatically. On the left-hand side, you can see all of the files that will make it into the commit, and exactly what was changed on each one.

## Commit your changes
Use the editor in the bottom-left of GitHub Desktop to write a summary and description for your changes.
- There is lots of guidance available for how to write these, but generally the summary should breifly describe the changes, and the description should explain why they were necessary
- https://easydynamics.sharepoint.com/sites/msd/SitePages/Git-Basics.aspx for more on writing good commits

## Push your changes to the remote
Double check the "history" tab and see what was committed. As of now, these changes still only exist on your local copy of the repository. You need to push to the remote for others to see these changes.
- Navigate to "publish branch"

## Open a pull request

## The pull request gets reviewed and merged

# Troubleshooting

## Switching between branches
You may be working on multiple branches at once. If you try to switch branches while changes are staged, you will be prompted to either keep the changes on the current branch, or bring them over to the branch you are switching to.
Be careful when switching branches, because GitHub Desktop gives the option to move changes from branch to branch with a single button click.
- Most likely, you will want to keep the changes on the current branch
- Selecting this option will STASH the changes
- Stashed changes will not appear in your text editor, but will be able to be popped out of the stash when you return to your original branch
- If you choose to bring your changes over to the new branch, those changes will become staged in that branch. Be careful doing this as it may lead to a merge conflict

## Amending commits

## Merge conflicts
Sometimes, you change a file in a way that git cannot automatically resolve those changes.
- This can happen if you bring changes over from a branch that has different history
- Git will try its best to neatly resolve changes, but likely you will encounter a manual merge conflict, as it appears here in Visual Studio:

## Force pushing
Sometimes, your local branch's history can get out of sync with its remote counterpart.
This can happen if you resolve a merge conflict or amend a commit and want those changes to exist on the remote copy of the feature branch. This will also happen if you make changes on an outdated version of the code.
- GitHub Desktop will prompt you with a warning if you try to push changes that require a force push
- Be VERY careful when force pushing. Only ever force push to your own feature branch - never a branch that others are working on
- Try to avoid needing to do this by keeping a neat commit history and keeping your local and remote branches in sync

# Where do I go to learn more?
- https://docs.github.com/en/get-started/learning-about-github/githubs-products
- https://docs.github.com/en/get-started/using-git/about-git
- Git courses on Linkedin Learning
