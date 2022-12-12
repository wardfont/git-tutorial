---
title: FNL Git tutorial
author: Ward Fonteyn
date: 13/12/2022 
---

## Why do we want to know?

Git is a **(collaborative) version control** software.

Git is the software on which GitHub, GitLab, Bitbucket, ... rely.

GitHub is where a lot of the software you use is maintained.

## Basic concept

![](./pictures/basic-concept.png)

## Let's try that

We will

- Make a new repository
- Add a remote GitHub repository to it
- Create files in our workspace
- Add them to our index
- Commit them to our local repository
- Push them to the remote on GitHub

## Credentials

```BASH
git config --global credential.helper store
git config --global user.email "your.email@email.com"
git config --global user.name  "Your name"
git config --global init.defaultBranch main
```

This will write your configurations in `~/.gitconfig` and your credentials in `~/.git-credentials`. Make sure the latter is never publicly available, it is not encrypted.


