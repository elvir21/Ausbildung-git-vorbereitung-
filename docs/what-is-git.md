# What is Git?

- [What is Git?](#what-is-git)
  - [What is Version Control?](#what-is-version-control)
  - [VCS hosting services](#vcs-hosting-services)

Git is the most commonly used version control system (VCS).
It is free and open sourced.

Git is a distributed VCS. This means that everyone who contributes to the project has a full copy (including the full project history) on their machine.

## What is Version Control?

A VCS tracks and manages changes to files over time in a repository (repo). A repo is the root folder of the project; the version control tracks all changes to files within it[^1].

- It keeps "snapshots" of the repository at various points in time.
- It remembers who changed what, at what time, and why.
- It can compare different versions of the same repository no matter where and when they happened.
- It provides the ability to "move back in time" and restore previous versions of the repository.

## VCS hosting services

Most repositories are hosted on Bitbucket, Github or other hosting services. This way, multiple people can contribute to a repo.

In this case, the copy of the repo that is located on the hosting service, is called `upstream repository`.

---

[^1]: You can exclude specific files and folders so that git will not track changes made to them. In Git, you do this with a `.gitignore` file.

[continue to 'Branches'](branches.md)
