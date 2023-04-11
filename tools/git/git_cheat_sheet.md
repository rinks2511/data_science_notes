# Git Cheat Sheet

## Getting Started
- `git init`: initialize a new repository
- `git clone <repository>`: clone an existing repository

## Staging Changes
- `git add <file>`: add changes to the staging area
- `git add -A`: add all changes to the staging area
- `git reset <file>`: unstage changes
- `git diff`: show unstaged changes
- `git diff --staged`: show staged changes

## Committing Changes
- `git commit -m "<message>"`: commit staged changes with a message
- `git commit --amend`: amend the previous commit with staged changes
- `git log`: show commit history

## Branching
- `git branch`: list branches
- `git branch <branch-name>`: create a new branch
- `git checkout <branch-name>`: switch to a branch
- `git merge <branch-name>`: merge changes from another branch
- `git branch -d <branch-name>`: delete a branch

## Pushing and Pulling
- `git remote add <remote-name> <remote-url>`: add a remote repository
- `git push <remote-name> <branch-name>`: push changes to a remote branch
- `git pull <remote-name> <branch-name>`: pull changes from a remote branch

## Other Useful Commands
- `git status`: show the status of the working tree
- `git stash`: stash changes for later use
- `git stash apply`: apply stashed changes
- `git rm <file>`: remove a file from the repository and the working tree
- `git mv <file> <new-file>`: rename a file in the repository and the working tree

This is just a basic cheat sheet, and there are many more Git commands and options available. It's always a good idea to consult the official Git documentation or additional resources for more information.