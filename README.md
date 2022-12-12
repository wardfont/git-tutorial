---
title: "A short introduction to git going"
author: "Ward Fonteyn"
date: "13/12/2022"
output:
  ioslides_presentation: default
  slidy_presentation: default
  beamer_presentation: default
---

# Git


## Why do we want to know?

Git is a **(collaborative) version control** software.

Git is the software on which GitHub, GitLab, Bitbucket, ... rely.

GitHub is where a lot of the software you use is maintained.

## What I do with IT

- Backup my coding, notes and pdfs (version control only works for plain text files)
- Searching through old code
- Looking at the source code of R-packages
- Raising issues to the developers of R-packages

## Basic concept

![](./pictures/basic-concept.png)

Files that are not yet added are **Untracked**. Files that are added, but have changed, have **Unstaged** changes.

## Let's try that

We will:

- Make a new repository
- Add a remote GitHub repository to it
- Create files in our workspace
- Add them to our index
- Commit them to our local repository
- Push them to the remote on GitHub

## Credentials

```bash
git config --global credential.helper store
git config --global user.email "your.email@email.com"
git config --global user.name  "Your name"
git config --global init.defaultBranch main
```

This will write your configurations in `~/.gitconfig` and your credentials in `~/.git-credentials`. Make sure the latter is never publicly available, it is not encrypted.

On GitHub, from your profile pictures, go to settings, choose "Developer options", "Personal access tokens", "Tokens (classic)", and choose "Generate new token (classic)".

Give it a relevant name (e.g. device you are using), set the desired expiration, and check the "repo" box. Create the token and copy and paste it somewhere for later.

## User interface

Git can be used either through:

- A command line interface
- A graphical user interface

We start with the command line interface, because it demystifies what is happening underneath.

## Help!

Open Git Bash.

`git` is the command which does all the work. If you want more information on what this command can do and how you can use it:

```bash
git --help
```

## init

Create a new directory, and in that directory right click and choose the option "Git Bash here"

```bash
git init
```

This turns your workspace into a git repository and creates a `.git` directory to store all git related files.

## status

```bash
git status
```

Check the status of your git repository.

## Create a readme file

```markdown
# This is a title

## This is a heading

This is text.

## This is another heading

This is some other text.
```

## add

We can now add the file to our index. It is not yet part of our git repository.

```bash
git add filename
```

or, if you want to add everything:

```bash
git add .
```

You can also remove files from your index using `git rm`.

## commit

Once we have a set of changes that we want to commit to our git repository, make sure all is correct using `git status`, then:

```bash
git commit
``` 

! This will open a terminal text editor ! 
Most likely vi(m). If you want to exit: ESC and ":q"

If you want to avoid using a terminal text editor:

```bash
git commit -m "my message"
``` 

Make sure to keep this message short.

## Creating and adding a remote repository

On GitHub, click on the "+" next to your profile picture, and create a new repository. Choose a name, write a description, and set if you want it to be public or private.

Once created, you get two code snippets: one for if you want to clone this new repository, the other one for if you want to push an existing repository. We choose the second option. 

Copy the code snippet and paste it in Git Bash. In command line environments, you can paste using "Ctrl-Shift-C" and "Ctrl-Shift-V". Press enter.

## push

Now that we have a remote repository, we can push our local repository to it:

```bash
git push
```

Check on GitHub if your push got through.

## fetch & pull

If your remote repository has changes, you can use `git fetch` to see what those changes are. If you want to integrate those changes in your local workspace, you can use `git pull`.

## Using a GUI

In Rstudio: New project from existing directory we just created.

You will see a Git tab in the top right panel.

There are a lot of different ways to interact with git, but they do the same thing as we did in the command line.

## Other features of Git

- Cloning
- `.gitingore`
- Merging
- Branching

# GitHub

## Github

"Where the world builds software"

- Easy searching
- Issues

## Searching code

You can see all the code from your favourite R package, or your own project.

Search through all their code and history.

## Issues

Like StackOverflow, but more up-to-date, and it's the developer answering.

# Git: Multiplayer Notepad


The end
