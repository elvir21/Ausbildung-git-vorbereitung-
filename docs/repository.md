# Setting up a repository

- [Setting up a repository](#setting-up-a-repository)
  - [Forking a repo](#forking-a-repo)
    - [What is a fork?](#what-is-a-fork)
    - [How to fork](#how-to-fork)
  - [Repo from scratch](#repo-from-scratch)
    - [Connecting a local repository](#connecting-a-local-repository)
  - [Exercise](#exercise)

## Forking a repo

### What is a fork?

You can fork a repository to create a copy of the repository and make changes
without affecting the original project.

Usually, you fork a repo when you

- want to propose changes but you do not have writing access for that project.
- want to use that repo as a basis for your own project.

*For this training, you will fork this repository to use it as a basis
for your own notes on working with Git.*

### How to fork

Usually, you can fork a repo via the interface of the repo's hosting service.
In this case, the repository is hosted on the company's bitbucket space and
you most likely do not have the rights to create repositories yourself.

1. **clone the repository**  
   Open the repository on Bitbucket, hit the "clone" button in the sidebar and copy the SSH url.
   To clone using the Terminal, run `git clone <repo> <directory>`.
   To clone using your GUI, open the Fork and select `File > Clone...`.
   Define the location and test the connection. Then `Clone` the repository.

2. **check the current remotes**  
   You can check where the remote (origin) of the repo is currently at by running
   the command `git remote -v` (the `-v` flag stands for verbose). It should look like this:  

   ```bash
   origin  ssh://git@bitbucket.hmmh.de:29418/u3uiws/ausbildung-git.git (fetch)
   origin  ssh://git@bitbucket.hmmh.de:29418/u3uiws/ausbildung-git.git (push)
   ```

3. **update origin**  
   Since you do not want to alter the original repository,
   create a new empty repo on the hosting service of your choice to host your copy there.
   Once you're done, copy the link to your new repo.
   Back in the terminal, update the origin to your repo by running the command

   ```bash
    git remote set-url origin git@{your-hosting-service}:{user-identification}/{repo-name}
   ```

   If you check your remotes again, the origin path should have been updated.

4. **configure upstream repo**  
   To keep the connection to the original repository and get its latest changes,
   we can configure another remote - the upstream.
   You can add it by running the command

   ```bash
    git remote add upstream git@bitbucket.hmmh.de:29418/u3uiws/ausbildung-git.git
   ```

   If you check your remotes again, you should see both the origin - pointing to your fork -
   and the upstream - pointing to repo on the company's bitbucket.

>If you can fork a repo via the interface, these are the steps you need to take:
>
>1. fork via interface
>2. clone your fork
>3. check the remotes  
    *(ensure the origin is set to your fork)*
>4. configure the upstream remote

## Repo from scratch

To start VC with git, simply run `git init` in the root directory of the project.
*Et voilà*, git will now locally track all changes made within that folder.

If you want to host a repository, you need to create a repo on the hosting service.
Depending on when you take that step, you will need do different things to host a repository.

When you create a repository, you always need to define the owner (space) of the repository, the name and the visibility.
Most hosting services provide options to automatically create common files, like a README.
If you create an empty repository, most hosting services will list all the options you now have to fill the repo with the files you need; follow them.

For your convenience, find the necessary steps to connect a local repository below.

**If you have any questions or need support, don't hesitate to ask your colleagues.**

### Connecting a local repository

If you already have a local repository, you have to add a remote origin.
You can do so by copying the remote url and running the command

```bash
git remote add origin {url-to-remote-repo}
```

The URL will look like this: `git@{your-hosting-service}:{user-identification}/{repo-name}`.

If you haven't set up a branch yet, you can move all of your current changes to a new branch
by running `git branch -M {branch-name}`. It's best practice to use `main` as your default branch.

Finally, push the branch to the upstream/origin repository by running `git push -u origin {branch-name}`.

Don't forget to commit your changes, if you haven't already.
(For more information on commit and pushing see later chapters.)

## Exercise

Fork this repo (or create a new one).
We will use the repo for exercises in this training.
