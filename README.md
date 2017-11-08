# Git & GitHub

![Rick&Morty](https://media.giphy.com/media/DgLsbUL7SG3kI/giphy.gif)


## Pre-requisites 🤘🏾 ✔️

- Have a Github/Github account.
- Have Git Bash installed.
- Speak a little English 😀

## Objectives 🚀

1. Take a deep breath.
2. Be able to navigate through the command line.
3. Explain the difference between git and GitHub.
4. Explain basic git commands like init, add, commit, push, pull and clone.
5. Describe the flow of forking and cloning.
6. Distinguish between local and remote repositories.
7. Create, copy, and delete repositories locally, or on GitHub.

### What is GitHub?

GitHub is a social network and user interface built on top of git. It's important to remember that you can use git without GitHub, but for our purposes, we'll almost always be managing our git repositories with the instance of GitHub.

### What is Git?

Git is a version control system. It allows developers to keep track of every single change they make to their code. It also lets you add comments, called commit messages, each time you make a change.

There's a lot of terminology involved in git. There's a lot of terminology involved in a most programming related things but git especially so. The following is a list of the most important concepts, for now. We'll learn some more advanced stuff as we go. (curated from [GitHub Glossary](https://help.github.com/articles/github-glossary/)):


## Git Basics

### Initializing a git repo (instructor demo)

Create a folder on your desktop called `TC_Git_Practice` using the `mkdir` command

Create a new directory in `TC_Git_Practice` called `test1`

You can turn any directory into a git repository by running the command `git init`.

Everything we do, that is, any changes we make to the files in `test1` can now be tracked by git. `test1` is a git repo, sometimes you'll hear it referred to as the working directory.

###  Creating a file in the repo, making some changes, and committing them (instructor demo)

We can create a new file in `test1` by running `touch newfile1.txt`. Make sure you're still in the `test1` directory first.

Open up `newfile1.txt` in your text editor (Visual Studio Code) and type some stuff in it.

To add these changes to our git history, run `git add -A` and the `git commit -m "your git message here"`. For the first commits of any project, convention is to name that commit "initial commit".

As we said earlier, adding and committing is like a two-step save process.

You can add everything that's been changed since the last commit by using the period, as in `git add .` or you can add specific files by specifying them, as in `git add newfile2.txt`

## Lab #1 (5-10 mins)

1. Create a new directory under `~/desktop/TC_Git_Practice` called `test2`
2. Initialize a git repo
3. Add some files
4. Make some changes to the files
5. Add the files
6. Commit the files
7. Repeat steps 3-4, in between each step run `git status` and `git log`. Try to summarize in a sentence what those two commands are doing.

## Pushing a repo to GitHub (instructor demo)

Create a new repo on [GitHub](https://help.github.com/articles/create-a-repo/)

After creating the repo GitHub is nice enough to give us some direction regarding how we get the repos *on our computer* sent, or pushed, to GitHub. Since `test1` already exists, we can follow the second set of directions.

`git remote add origin https://github.com/[your-username]/test1.git`
`git push -u origin master`

Adding the *remote* tells our repo that a copy of it lives somewhere else (GitHub). This gives us the ability to make changes on our *local* repo, and then send them to the one on GitHub.

To make changes and send them up to GitHub we would add, commit, and then *push* them like so: `git push`

## Forking and Cloning

To fork a repo on GitHub, navigate to the repo you want to fork and click the fork button.

Once it's been forked, you can go to your GitHub account and click the clone button. There should be a URL. Copy and paste the one that begins with `https://`

Run the following command in the directory that you want to clone the repo. You should never ever ever ever ever clone a repo inside another repo.

`git clone https://github.com/[your-username]/fakereponame.git`

Now that the repo has been cloned you can make changes locally. Once you've done that you can add, commit and, push the changes back to the remote.

## Commit messages

Make sure your commit messages describe what changes you've made. If a commit history looks like this:

Bad: Fix stuff
Good: Fixed mobile navbar.

### *in general, you should be able to say "this commit will" and then read the commit message and everyone will know exactly what the commit accomplished*

## Opening a Pull Request (Code Along)
1. Fork this repo.
2. Clone this repo.
3. Create changes to it. (Edit the editme.txt file)
4. Git add/commit/push
5. Go to original repo and click "New Pull Request"

## Markdown and READMEs

If your repo has a readme.md then GitHub will display it on the repo's homepage.

This page you're looking at now was written in Markdown language.

[Everything you need to know about Markdown.](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)

## Conclusion (5 mins)
- Repeat once again: 'I will not clone a repo in a repo'
- Difference b/t forking and cloning
- What is a pull request?
- How to initialize a git repo?

## Resources

1. [Git Cheat Sheet # 1](https://www.git-tower.com/blog/git-cheat-sheet/)
2. [Git Cheat Sheet # 2](http://alvinalexander.com/git/git-cheat-sheet-git-reference-commands)
3. [Markdown Cheat Sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Important Terms:

1. **Git**:
    - an open source program for tracking changes in text files. It is the core technology that GitHub, the social and user interface, is built on top of.
2. **Repository**:
    - they're easiest to imagine as a project's folder. A repository contains all of the project files (including documentation), and stores each file's revision history.
    - A codebase in Git is referred to as a repository, or repo, for short.
3. **Fork**:
    - a personal copy of another user's repository that lives on your account. Forks allow you to freely make changes to a project without affecting the original. Forks remain attached to the original, allowing you to submit a pull request to the original's author to update with your changes. You can also keep your fork up to date by pulling in updates from the original.
    - Pull Request: When you want to propose a change to a repository (the original project) that you have forked, you can issue a pull request. This basically is you saying:
    "I've made some changes to your repository, if you want to include them in your original one then you can pull them from my fork!"
4. **Clone**:
    - a copy of a repository that lives on your computer instead of on a website's server somewhere, or the act of making that copy. With your clone you can edit the files in your preferred editor and use Git to keep track of your changes without having to be online. It is, however, connected to the remote version so that changes can be synced between the two. You can push your local changes to the remote to keep them synced when you're online.
5. **Pull**:
    - refers to when you are fetching in changes and merging them. For instance, if someone has edited the remote file you're both working on, you'll want to pull in those changes to your local copy so that it's up to date.
6. **Add**:
    - adds a change in the working directory to the staging area. It tells Git that you want to include updates to a particular file in the next commit. However, git add doesn't really affect the repository in any significant way—changes are not actually recorded until you run git commit.
7. **Commit**:
    - an individual change to a file (or set of files). It's like when you save a file, except with Git, every time you save it creates a unique ID (a.k.a. the "SHA" or "hash") that allows you to keep record of what changes were made when and by who. Commits usually contain a commit message which is a brief description of what changes were made. *You can thinking of adding and committing as a two-step saving process.*
8. **Push**:
    - refers to sending your committed changes to a remote repository such as GitHub.com. For instance, if you change something locally, you'd want to then push those changes so that others may access them.
9. **Branch**:
    - a parallel version of a repository. It is contained within the repository, but does not affect the primary or master branch allowing you to work freely without disrupting the "live" version. When you've made the changes you want to make, you can merge your branch back into the master branch to publish your changes.
10. **Merge**:
    - takes the changes from one branch (in the same repository or from a fork), and applies them into another. This often happens as a Pull Request (which can be thought of as a request to merge), or via the command line. A merge can be done automatically via a Pull Request via the GitHub.com web interface if there are no conflicting changes, or can always be done via the command line.
11. **Reset**:
    - can undo commits to go back in time to a particular commit.
