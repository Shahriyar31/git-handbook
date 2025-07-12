# Git Command Reference Cheatsheet

A quick reference for the most common and useful Git commands, from basic to advanced.

---

### Setup & Initialization
| Command | Description |
|---|---|
| `git init` | Initializes a new Git repository in the current directory. |
| `git clone <url>` | Creates a local copy of a remote repository. |
| `git config --global user.name "Name"` | Sets your name for all commits. |
| `git config --global user.email "email"` | Sets your email for all commits. |

---

### The Basic Workflow (Staging & Committing)
| Command | Description |
|---|---|
| `git status` | Shows the status of your working directory and staging area. |
| `git add <file>` | Adds a specific file to the staging area. |
| `git add .` | Adds all new and modified files to the staging area. |
| `git commit -m "Message"` | Saves staged changes to your local history with a message. |
| `git commit -am "Message"` | Stages all *tracked* files and commits them in one step. |

---

### Branching & Merging
| Command | Description |
|---|---|
| `git branch` | Lists all local branches. `git branch -a` lists all branches. |
| `git branch <branch-name>` | Creates a new branch. |
| `git switch <branch-name>` | Switches to an existing branch (modern method). |
| `git switch -c <branch-name>` | Creates a new branch and switches to it. |
| `git merge <branch-name>` | Merges the specified branch into your current branch. |
| `git branch -d <branch-name>` | Deletes a local branch (only if it has been merged). |

---

### Remote Operations
| Command | Description |
|---|---|
| `git remote -v` | Lists all your remote connections. |
| `git fetch` | Downloads changes from the remote, but doesn't integrate them. |
| `git pull` | Fetches changes from the remote and merges them into your current branch. |
| `git push` | Pushes your local committed changes to the remote repository. |
| `git push -u origin <branch>` | Pushes a new branch and sets its upstream tracking link. |

---

### Inspection & History
| Command | Description |
|---|---|
| `git log` | Shows the commit history for the current branch. |
| `git log --oneline` | Shows the commit history in a condensed, one-line format. |
| `git diff` | Shows unstaged changes between your working directory and staging area. |
| `git diff --staged` | Shows staged changes between your staging area and your last commit. |

---

### Undoing Changes
| Command | Description |
|---|---|
| `git restore <file>` | Discards unstaged changes in a specific file. |
| `git restore --staged <file>` | Unstages a file, moving it back to the working directory. |
| `git commit --amend` | Replaces the very last commit with a new one. |
| `git reset <commit>` | Resets `HEAD` to a previous commit, keeping changes in the working directory. |
| `git reset --hard <commit>` | **DANGEROUS:** Resets `HEAD` and discards all changes since that commit. |
| `git revert <commit>` | Creates a new commit that undoes the changes of a previous commit. |

---

### Advanced & Other
| Command | Description |
|---|---|
| `git rebase <branch>` | Re-applies commits from the current branch on top of another branch. |
| `git stash` | Temporarily saves uncommitted changes. |
| `git stash pop` | Applies the most recently stashed changes and removes them from the list. |
| `git cherry-pick <commit>` | Applies a single commit from another branch onto your current branch. |
| `git tag -a v1.0 -m "Message"` | Creates an annotated tag for marking a release. |
| `git reflog` | Shows a log of all actions taken in the repo (your safety net). |
