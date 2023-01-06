# What is Git?
	- the industry standard distributed version control system

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

## Enter Git:
	- Git organizes your code into commits, which are atomic sets of changes to the code.
	- A commit looks like this:
		- File diff, author, timestamp, previous change hash
	- Git will store these commits as a log that looks like this:
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

#Demo time

## Clone a repository

## Create a branch

## Write some code

## Stage the files you changed

## Commit your changes

## Check the status

## Push your changes to the remote

## Open a pull request

## The pull request gets reviewed and merged

# Where do I go to learn more?
- https://docs.github.com/en/get-started/learning-about-github/githubs-products
- https://docs.github.com/en/get-started/using-git/about-git
- Git courses on Linkedin Learning
