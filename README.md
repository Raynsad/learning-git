# What is Git?
The industry standard distributed version control system

## What problem does it solve?
- Alice and Bob are working on a project together for school
- They need to share code and turn it in
- They don't know the proper way to do this, so they paste their code in a Google Doc
- They code on the same file at the same time

### Problem 1:
- Alice and Bob copy the Google Doc into their own IDE's
- They both make changes separately
- Some secret tests are passing in Alice's environment, and others are passing in Bob's environment
- They cannot tell which parts of the code were written by who, nor can they merge the two versions together without a ton of effort

### Problem 2:
- The night before submitting the project, both Alice and Bob make changes to different parts of the code
- They compile the code and the program breaks. They want to go back to an old version to try and fix the breaking changes
- How do they revert JUST the breaking changes?
- They can't

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

## Create a branch
### What is a branch?
- A version of the source code within the repository
- Each branch contains its own history of commits
- Typically, a branch is used for individual development and then merged into a main branch
- When you create a branch for the purpose of making a change, adding a feature, or fixing an issue, it is called a feature branch.

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


## Check the status

## Push your changes to the remote

## Open a pull request

## The pull request gets reviewed and merged

# Basic Troubleshooting

## Switching between branches

## Amending commits

# Where do I go to learn more?
- https://docs.github.com/en/get-started/learning-about-github/githubs-products
- https://docs.github.com/en/get-started/using-git/about-git
- Git courses on Linkedin Learning
