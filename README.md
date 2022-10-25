# Git Training

- ... covers the basics of Git and how to work with it.
- ... includes examples for Git's command line interface (CLI) and the Git GUI [Fork](https://git-fork.com/).
- ... lists useful Visual Studio Code (VS Code) extensions.

## Prerequisites

1. Set up an account on the company's Bitbucket (or another Version Control System (VCS)).
2. Set up [Fork](https://git-fork.com/) or another Git GUI.
3. Set up a personal account on a VCS (e.g. GitHub).
4. Create an SSH key and connect it to your Bitbucket and GitHub accounts and GUI.
5. Install and setup VS Code (or another IDE).

## Table of Contents

- [What is Git?](docs/what-is-git.md)
- [Repository](docs/repository.md)
- [Branches](docs/branches.md)
  - What is a branch and what does it do?
  - Local vs remote branches
  - Working with branches (`git branch` & `git checkout`)
- [Workflow: Making changes](docs/workflow-making-changes.md)
  - Staging changes (`git add`)
  - Keeping an overview
    - Status of current changes (`git status`)
    - History (`git log`)
    - Details per line (`git blame`)
  - Committing changes (`git commit`)
    - Amending changes to previous commits (`--amend`)
  - Stashing changes (`git stash`)
  - Comparing changes (`git diff`)
  - Reset (`git reset`) *#advanced*
  - Revert (`git revert`) *#advanced* *#caution (ask a peer for support)*
- Workflow: Synchronizing changes
  - Fetch vs Pull (`git fetch` & `git pull`)
  - Push & Force Push (`git push`)
  - Rebase (`git rebase`)
  - Dealing with merge conflicts
  - Tags (`git tag`)
  - Cherry picking (`git cherry-pick`)
- Best Practices
  - Git-flow
  - Conventional commits
  - VS Code extensions
- [Glossary](docs/glossary.md)

## Further resources

- [Learn Git Branching](https://learngitbranching.js.org/)
: an interactive tutorial in the **browser** for working with Git
- [Oh My Git!](https://ohmygit.org/)
: a game for learning git
- [Git's guide](https://git-scm.com/book/en/v2)
: the official written guide - very detailed, also available in [German](https://git-scm.com/book/de/v2) and other languages
- [Atlassian's guide](https://www.atlassian.com/git/tutorials/setting-up-a-repository)
: a written guide with many examples
