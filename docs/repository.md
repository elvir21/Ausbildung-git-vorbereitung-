# Setting up a repository

- [Setting up a repository](#setting-up-a-repository)
  - [Forking a repo](#forking-a-repo)
    - [What is a fork?](#what-is-a-fork)
    - [How to fork](#how-to-fork)
  - [Repo from scratch](#repo-from-scratch)
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
n this case, the repository is hosted on the company's bitbucket space and
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

tbd

## Exercise

Fork this repo (or create a new one).
We will use the repo for exercises in this training.
