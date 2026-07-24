<!-- # Intro to Git and github -->

# Git

### what is git ?

**Git** is a version control tool created by Linus Torvalds on April 7, 2005 for the development of Linux kernel

### What is version control ?

**Version control** is a system for tracking changes to files over time. It lets you record snapshots of your work, revisit earlier versions, collaborate with others, and safely experiment without losing progress.

Git manages the history of your project by storing a series of commits (snapshots) and providing tools to compare, merge, and restore changes.

### When is it useful?

without using version control you will have to save same files with different names just to manage them.  
**eg:**

* `main.c`
* `main_v2.c`
* `main_final.c`
* `main_final_v2.c`

Now imagine this for project of 5,10, 20 files.  
Git avoids by saving these versions as commits, where each commit saves your entire code base as **commits**

## Git structure

Main structures of git is:

* [Repository](#repository)
* [Commit](#git-commit)
* [Branch](#git-branch)

### Repository
A Git repository (or repo) is a project that Git tracks.

It contains:

* Your project files (source code, documentation, images, etc.)
* A hidden `.git` directory that stores the project's complete history and metadata.

```
            Git Repository
    +-----------------------------+
    |                             |
    |  Project Files              |
    |  ├── app.py                 |
    |  ├── README.md              |
    |  └── package.json           |
    |                             |
    |  .git/                      |
    |  ├── commits                |
    |  ├── branches               |
    |  ├── tags                   |
    |  └── configuration          |
    |                             |
    +-----------------------------+
```

### Git commit

A commit is a snapshot of your project at a specific point in time. Instead of saving the project as "version1", "version2", and "version3", Git stores commits.  
**eg:**

```
Commit A
│
├── Initial project
│
▼
Commit B
│
├── Added login
│
▼
Commit C
│
├── Fixed bug
│
▼
Commit D
│
└── Added dashboard
```

### Git branch

Branches are like parallel universe for your code. Branches allow you to work on project code without affecting the **main** branch.

```
                     Commit A
                         │
                         ▼
                     Commit B
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
           main              login-feature
              │                     │
              ▼                     ▼
          Commit C             Commit X
              │                     │
              ▼                     ▼
          Commit D             Commit Y
```

## Git workflow

### How to set up a local repository

Git repo is created on your project directory. Open your project directory in terminal and use these commands:

* `git init` - this creates a local repository
* `git add .` - this adds all the files on that folder and subfolder to the repository. You can use `git add file1 file2 file3` to add specific files where *file1*, *file2* are the names of your actual files.
* `git commit -m "commit message"` - this commits (saves) your file to your local repo (replace the *commit message* with useful message)
* `git push` - this saves your commit in local repo to Github repo

```
            Edit Files on
        Working Directory
                 │
          git add
                 │
                 ▼
          Staging Area
                 │
        git commit
                 │
                 ▼
       Local Repository
                 │
         git push
                 │
                 ▼
       GitHub Repository
```

## Github

[Github](https://github.com/) is a website owned by Microsoft to store all your codebase in the cloud. It helps you upload your code in your own local machine (pc, laptop etc) to the internet (github server) so you can access your code from other's machines

### Git vs GitHub

Although the names sound similar, **Git** and **GitHub** are different.

| Git | GitHub |
|------|---------|
| Git is a **Version Control System (VCS)**. | GitHub is a **cloud-based hosting platform** for Git repositories. |
| It tracks changes made to your project. | It stores Git repositories online. |
| Works locally on your computer. | Works on the internet (cloud). |
| Can be used without an internet connection. | Requires an internet connection to sync repositories. |
| Developed by **Linus Torvalds** in 2005. | Founded in 2008 and now owned by Microsoft. |
| Installed as software on your computer. | Accessed through a web browser or [GitHub Desktop](https://github.com/apps/desktop). |
| Used to create commits, branches, and manage project history. | Used to share projects, collaborate with others, review code, and back up repositories. |

#### Simple Analogy

Think of writing a document.

- **Git** is like the **Save** feature in your editor—it keeps track of every version of your document.
- **GitHub** is like **Google Drive**—it stores your document online so you can access it anywhere and collaborate with others.


```text
                Your Computer

            +------------------+
            |      Git         |
            |------------------|
            | Tracks changes   |
            | Saves commits    |
            | Manages history  |
            +------------------+
                    |
               git push
                    |
                    ▼
          +----------------------+
          |       GitHub         |
          |----------------------|
          | Stores repositories  |
          | Online backup        |
          | Collaboration        |
          +----------------------+
```

- **Git** = A tool that tracks and manages your project's history.
- **GitHub** = A website that stores Git repositories online and makes collaboration easy.

> **Note:** Git can work without GitHub, but GitHub cannot work without Git repositories managed by Git.
