**Git Cheat Sheet**

---

### 1. Setup & Configuration

- **`git config --global user.name "Your Name"`** – Set your name (appears in commits).
- **`git config --global user.email "you@example.com"`** – Set your email.
- **`git config --list`** – Show current config settings.

### 2. Creating a Repository

- **`git init`** – Initialize a new Git repository in the current folder.
- **`git clone <url>`** – Copy an existing remote repo to your machine.

### 3. Basic Workflow

| Action                                 | Command                         | What it Does                                              |
| -------------------------------------- | ------------------------------- | --------------------------------------------------------- |
| **Check status**                       | `git status`                    | Shows staged, unstaged, and untracked files.              |
| **Stage files**                        | `git add <file>` or `git add .` | Adds changes to the staging area.                         |
| **Commit**                             | `git commit -m "Message"`       | Saves staged changes with a descriptive message.          |
| **Combine add & commit**               | `git commit -am "Message"`      | Stages _tracked_ files and commits in one step.           |
| **View history**                       | `git log`                       | Shows commit history. Add `--oneline` for a compact view. |
| **Undo last commit (keep changes)**    | `git reset --soft HEAD~1`       | Moves HEAD back but leaves changes staged.                |
| **Undo last commit (discard changes)** | `git reset --hard HEAD~1`       | Deletes the commit and its changes.                       |

### 4. Branching

- **`git branch`** – List all branches.
- **`git branch <name>`** – Create a new branch.
- **`git checkout <branch>`** – Switch to a branch.
- **`git checkout -b <name>`** – Create and switch to a new branch in one step.
- **`git merge <branch>`** – Merge the specified branch into the current one.
- **`git branch -d <branch>`** – Delete a branch (must be merged).

### 5. Remote Repositories

- **`git remote -v`** – Show remote URLs.
- **`git remote add origin <url>`** – Add a new remote named “origin”.
- **`git push`** – Upload local commits to the remote (default: current branch).
- **`git push origin <branch>`** – Push a specific branch.
- **`git pull`** – Fetch and merge changes from the remote.
- **`git fetch`** – Download remote changes without merging.

### 6. Inspecting Changes

- **`git diff`** – Show unstaged changes.
- **`git diff --staged`** – Show staged changes.
- **`git show <commit>`** – Display details of a specific commit.

### 7. Stashing (temporary storage)

- **`git stash`** – Save current work-in-progress changes.
- **`git stash list`** – List saved stashes.
- **`git stash apply`** – Reapply the most recent stash.
- **`git stash pop`** – Apply and remove the most recent stash.

### 8. Undoing Changes

- **`git checkout -- <file>`** – Discard changes in a file (restore last committed version).
- **`git revert <commit>`** – Create a new commit that undoes a previous one.

### 9. Tagging

- **`git tag`** – List tags.
- **`git tag -a v1.0 -m "Release 1.0"`** – Create an annotated tag.
- **`git push origin --tags`** – Push tags to the remote.

### 10. Common Helpful Options

- **`-v`** – Verbose output (e.g., `git status -v`).
- **`--all`** – Operate on all refs (e.g., `git push --all`).
- **`--force`** – Force push (use with caution).

---

#### Quick Reference Commands

```
git init               # start a repo
git clone <url>        # copy remote repo
git status             # view repo state
git add .              # stage all changes
git commit -m "msg"    # commit
git log --oneline      # view concise history
git branch             # list branches
git checkout -b new    # create & switch branch
git merge other        # merge branch
git push               # send commits
git pull               # fetch & merge
git stash              # save work temporarily
git stash pop          # restore stashed work
```
