###### Forenote 

---

# Git 

## Resources 

* [About Git](https://git-scm.com/about)
* [Pro GitBook](https://git-scm.com/book)
* [Reference Documentation](https://git-scm.com/docs)

## Chapter 1 - Getting started

* VCS (Version Control System) - Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later.

* Allows you to revert selected files back to a previous state, revert the entire project back to a previous state, compare changes over time, see who last modified something that might be causing a problem, who introduced an issue and when, and more. Using a VCS also generally means that if you screw things up or lose files, you can easily recover. In addition, you get all this for very little overhead.

## Chapter 2 - Git Basics 

* Chapter Objectives
  * Configure and Initialize a Repository
  * Begin and Stop Tracking Files
  * Stage and Commit changes 

### Getting a Git Repository

1. Turn local directory not under version control into a git repository(``git init``)
2. Clone/Copy an existing repository

### Initializing a Repository in an Existing Directory

* Running ``git init`` in a directory not under version control will create a directory called ``.git`` containing repository files, initializing the directory as a git repository.
*  *NOTE* - See [sidenote](###What Happens If I run Git Init Twice?) on what happens if you run ``git init`` in an already initialized repository.

### Cloning an Existing Repository

* ``git clone`` copies an existing repository e.g ``git clone https://github.com/libgit2/libgit2`` 
  * Initializes `.git` directory inside it, pulls all data and checks out a working latest working copy.
* Copies a full working copy with almost all data server has e.g every version for all files. 
* via HTTPS, SSH, [etc.](https://git-scm.com/book/en/v2/ch00/_getting_git_on_a_server) 

## Sidenotes 

### Concepts And Their Purposes

### SCM= 

* Source Code Management when talking about source code. 
* If keeping config files (things in /etc, application-specific config files, etc.) in an SCM, then = Software Configuration Management.

### What Happens If I run Git Init Twice?

### License 

https://choosealicense.com/

