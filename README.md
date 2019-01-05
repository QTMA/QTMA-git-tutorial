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
Now let's dive in! Press the "Fork" button in the top right corner of this repository.
![Fork Image](assets/img/fork-screenshot.png)
This will produce a copy of the repository on your own GitHub account. This is a
common practice for open source projects, or other projects where you don't have
edit permission on the main repository. You'll be making changes in your own copy,
then submitting a "pull request" to propose changes to the main repository - more
on that later.

Next, we'll create a local copy of the repository on your machine. Navigate to your
own copy of the repo on GitHub, press the "Clone or download" button, and copy the
resulting URL. Next, open a Command Prompt or Terminal, navigate to the parent
directory where you want your repo to be stored, and type the following:
```
$ git clone https://github.com/your-username/QTMA-git-tutorial.git
$ cd QTMA-git-tutorial
```
In addition to creating a copy of the repository on your machine, the `clone`
command also links it to your repository on GitHub. This is called a "remote",
and it has been named "origin". This allows you to send and receive changes to
your copy of the repo on GitHub. But what about changes being made to the original
repository? We can add another remote, which we'll call "upstream", pointing
the main repository.
```
$ git remote add upstream https://github.com/QTMA/QTMA-git-tutorial.git
```
If you're working on a personal project or on a centralized team where everyone
has edit permission on the main repository, i.e. not open source, you can
forego the forking step and addition of a second remote and simply clone the
main repo directly to your machine.

## Branching
When multiple people are working on the same project, conflicts can arise if
people try to edit the same lines, someone deletes a file that someone else is using,
refactors a function in a breaking manner, etc. Branches allow you to keep a set
of commits separate from the main history, so that you don't need to worry about
other people's changes breaking yours, and vice versa while a feature is still under
development.

The `branch` command will create a new branch from whichever branch you are currently on.
Generally, we want to branch from master, which is the default branch, although there
are some workflows such as [GitFlow](https://nvie.com/posts/a-successful-git-branching-model/)
which use more complicated branching schemes. To view a list of branches, with the current
branch highlighted, use the following command:
```
$ git branch
```
After verifying that you're on master create a new branch to contain your feature
using `branch`, then switch to the new branch using `checkout`.
```
$ git branch <your-name>
$ git checkout <your-name>
```
Note that branches can be useful even when developing individually. If you are
developing multiple features concurrently, it can be helpful to separate the
development of each feature into its own branch in order to keep the main commit
history clean and organized.

## Making Changes
## Undoing Changes
## Getting Remote Changes
## Conflicts
## Pull Requests
