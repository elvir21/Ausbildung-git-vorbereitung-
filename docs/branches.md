# Branches

- [Branches](#branches)
  - [What is a branch and what does it do?](#what-is-a-branch-and-what-does-it-do)
  - [Local vs remote branches](#local-vs-remote-branches)
  - [Working with branches (git branch & git checkout)](#working-with-branches-git-branch--git-checkout)

## What is a branch and what does it do?

Branching offers a way to work on a new feature without affecting the main codebase.

Like a branch on a tree, a branch still belongs to the main codebase, the tree trunk.  
Like a tree, a repository can have many branches.  
Like on a tree, branches can grow on other branches.

When you create a branch, you start a line of work that will not affect what happens on its base branch. When you are done, you can create a merge that branch back to the base branch.

Usually, there are two main branches and multiple working branches in a repository.

The `main` (or `master`) branch usually tracks the state of the live application.  
The `develop` branch tracks the state of the fully developed and approved features.  
The working branches track the state of specific feature development, bug- or hotfixes.

## Local vs remote branches

Most of the time, the repository will be hosted on Github, Bitbucket, or other hosting services; especially when working with others. When you make changes, these are only visible to you until you push them to the remote repository. If other contributors make and push changes, you need to fetch or pull them to be able to see them.

Most GUIs, like the [Fork](https://git-fork.com/), will automatically fetch the repository periodically. Remote branches will be listed as `origin/{branchName}` and prefixed with an icon. If your local branch is in sync with the remote branch, only the icon will be shown in the tree view.  
In later chapters we'll explain how to keep local and remote branches in sync.

![local branch in sync with remote branch](../assets/docs/branches_local-remote-sync.JPG)  
*Remote and local branches in sync*

![local branch is one commit ahead](../assets/docs/branches_local-remote-local-ahead.JPG)  
*Local branch is one commit ahead*

![remote branch is one commit ahead](../assets/docs/branches_local-remote-remote-ahead.JPG)  
*Remote branch is one commit ahead*

If you do not use a GUI, you can list all local and remote branches with the command `git branch -a`.

## Working with branches (git branch & git checkout)

You can create a new branch either using the GUI or by running one of the following commands:

- `git branch {branch-name}`  
*Note that this command will only create the branch but will not check it out.*
- `git switch -c {branch-name}`
- `git checkout -b {branch-name}`

In the GUI right-click on the commit (either in the list or the tree-view) and select `New Branch...`.

If you want to checkout an existing branch, you can run one of the following commands

- `git checkout {branch-name}`
- `git switch {branch-name}`

---

[continue to 'Workflow: Making changes'](workflow-making-changes.md)
