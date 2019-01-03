# Learn Git and GitHub With QTMA
This workshop is designed to take you through a Git workflow that is commonly used  
for collaborative software development; however, much of this knowledge is applicable
when developing individually.

Note: code blocks where each line is preceded by `$`, like:
```
$ sudo apt-get update
$ sudo apt-get install git
```
are a stylistic convention used to display terminal commands. Do not enter the `$`
when copying these commands.

# Table of Contents
1. [Setup](#setup)
2. [Why Git](#why-git)
3. [Concept Overview](#concept-overview)
4. [Forking and Cloning](#forking-and-cloning)
5. [Branching](#branching)
6. [Making Changes](#making-changes)
7. [Undoing Changes](#undoing-changes)
8. [Getting Remote Changes](#getting-remote-changes)
9. [Conflicts](#conflicts)
10. [Pull Requests](#pull-requests)

## Setup
1. Create a [GitHub account](github.com)
2. Install Git
  - **Mac OS X** [Installer](https://sourceforge.net/projects/git-osx-installer/files/) or
    `brew install git` with Homebrew
  - **Windows** [Installer](https://git-for-windows.github.io/)
  - **Linux**
  ```
  $ sudo apt-get update
  $ sudo apt-get install git
  ```
3. Verify that the installation was successful with `git --version` in Terminal
or Command Prompt
4. Configure Git with the following commands in Terminal or Command Prompt.
This information will be attached to each commit you make.
```
$ git config --global user.name "Your Name"
$ git config --global user.username "yourusername"
$ git config --global user.email "youremail@email.com"
```

## Why Git
First, though, why version control? By using version control, you can progressively
save "snapshots" of your work and easily roll back to a "snapshot" if something
goes wrong. Additionally, these "snapshots" provide a history of development,
which will make the project more maintainable in the long run and can be highly
useful when adding new features or onboarding new team members. Lastly, version
control provides a way for multiple people, even tens of thousands at the scale
of companies like Google and Facebook, to contribute to the same codebase.

Git is one of the most commonly used version control systems, along with Mercurial
and SVN. It has become the industry standard for open source projects, which are usually
hosted on GitHub. Additionally, learning Git will allow you to share personal projects
on GitHub, which is a great way to show off your abilities to potential employers.

## Concept Overview
Git calls the "snapshots" discussed above "commits". You want to commit frequently
such that you have a complete and detailed history of development. However, each
commit should represent a unitary change - don't commit the way you save in Microsoft
Word. You should never commit half complete or broken code - add the class or complete
the function, then commit.

You don't have to add every changed file when you make a new commit. Git uses a
"staging area" which files are added to and then committed from. This allows for
much more flexibility when committing, and enables you to split your commits up
logically.

## Forking and Cloning
Now let's dive in! Press the fork button in the top right corner of this repository.
![Fork Image](assets/img/fork-screenshot.png)
This will produce a copy of the repository on your own GitHub account. This is a
common practice for open source projects, or other projects where you don't have
edit permission on the main repository. You'll be making changes in your own copy,
then submitting a "pull request" to propose changes to the main repository - more
on that later.

## Branching
## Making Changes
## Undoing Changes
## Getting Remote Changes
## Conflicts
## Pull Requests
