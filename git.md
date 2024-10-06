# Git and Github

Git is a distributed version control system design to track changes in the source code and other files over time. it allows multiple developers to work on a project simultaneously without conflicting with each other's changes.

## Table of Contents
1. [Creating a Repository](#1-creating-a-repository)
2. [Cloning a Repository](#2-cloning-a-repository)
3. [Creating Branches](#3-creating-branches)
4. [Committing Changes](#4-committing-changes)
5. [Reverting Commits](#5-reverting-commits)
6. [Pulling and Pushing Changes (Downstream and Upstream)](#6-pulling-and-pushing-changes-downstream-and-upstream)
7. [Fetching Changes](#7-fetching-changes)
8. [Merging Branches](#8-merging-branches)
9. [Renaming Branches](#9-renaming-branches)
10. [Creating Pull Requests](#10-creating-pull-requests)
11. [Reviewing and Merging Pull Requests](#11-reviewing-and-merging-pull-requests)
12. [Reverting Pull Requests](#12-reverting-pull-requests)

## 1. Creating a Repository 

A repository is where all the project's files and the revision history are stored. There are two ways to create a repository:

### Commands:
1. To create a new Git repository:
    ```bash
    git init
    ```
    This command initializes an empty Git repository in your current directory.

2. To create a repository from an existing project:
    ```bash
    git init
    git add .
    git commit -m "Initial commit"
    ```

## 2. Cloning a Repository

Cloning a repository allows you to copy an existing repository from a remote source, such as GitHub, to your local machine.

### Commands:
```bash
git clone <repository-url>
```


## 3. Creating Branches
Branches allow you to work on different features or bug fixes independently from the main codebase.

### Commands:
1. To create a new branch:

``` bash
git branch <branch-name>
```
2. To switch to a different branch:

``` bash 
git checkout <branch-name>
```
3. To create and switch to a new branch in one command:

```bash
git checkout -b <branch-name>
```

## 4. Comitting Changes

A commit is like saving  your progress in Git. it Snapshots the current state of your files. 

### Commands:
1. Stage Changes:
``` bash
git add <file name> # To add a specific file
git add . # To add all the changes
```
2. Commit staged Changes:
```bash
git commit -m "Commit message"
```

## 5. Reverting Commits

Reverting a commit means undoing changes made ina previous commit without altering the project history.

### Commands:
1. To revert a specific commit:
```bash
git revert <commit-hash>
```
The commit-hash is the unique identifier for the commit you want to revert.

## 6. Pulling and Pushing Changes (Downstream and Upstream)
Pulling refers to downloading changes from a remote repository to your local repository. Pushing refers to uploading your local changes to a remote repository.

### Commands:
1. To pull changes from a remote repository:

```bash
git pull origin <branch-name>
```
2. To push changes to a remote repository:

```bash
git push origin <branch-name>
```
## 7. Fetching Changes
Fetching allows you to see what others have committed to a remote branch without merging the changes into your working directory.

### Commands:
```bash
git fetch origin
```
## 8. Merging Branches
Merging integrates the changes from one branch into another.

### Commands:
1. First, switch to the branch where you want the changes:
```
bash
git checkout <branch-name>
```
2. Then, merge the changes from another branch:

```bash
git merge <branch-to-merge>
```
## 9. Renaming Branches
If you want to rename a branch for clarity or organizational purposes:

### Commands:
1. Rename the current branch:

```bash
git branch -m <new-branch-name>
```
2. Push the renamed branch to the remote repository:

```bash
git push origin -u <new-branch-name>
```
3. Delete the old branch reference on the remote:

```bash
git push origin --delete <old-branch-name>
```
## 10. Creating Pull Requests
Pull requests (PRs) allow developers to notify team members about changes they’ve pushed to a branch in a repository.

### Commands:
1. Push the branch you want to propose changes from:

```bash
git push origin <branch-name>
```
2. Navigate to the repository in a platform like GitHub and open a pull request from that branch to the main or any other branch.

## 11. Reviewing and Merging Pull Requests
After a pull request is created, team members can review the changes and approve or request changes.

### Steps:
1. In your GitHub/GitLab UI, navigate to the pull request.
2. Review the code changes.
3. Approve, request changes, or comment.
4. Once ready, merge the pull request.
## 12. Reverting Pull Requests
If a pull request introduces a bug or unwanted changes, you can revert it.

### Steps:
1. Navigate to the merged pull request on GitHub or GitLab.
2. Click the "Revert" button, which creates a new pull request that undoes the changes introduced by the original one.






