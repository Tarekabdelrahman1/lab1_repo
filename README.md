# Lab 1: Git & GitHub Workflow


## Commands Used

Below is the step-by-step order of commands used to complete this lab:

### 1. Repository Initialization & Setup
* `mkdir lab1_repo` - Created the project directory.
* `cd lab1_repo` - Entered the directory.
* `git init` - Initialized a new local Git repository.
* `touch code.py` - Created the Python script file.
* `echo 'print("Tarek Abdelrahman")' > code.py` - Added the full name to the file.

### 2. First Commit & Remote Connection
* `git add code.py` - Staged the file.
* `git commit -m "the first commit"` - Created the initial commit.
* `git remote add origin git@github.com:Tarekabdelrahman1/lab1_repo.git` - Linked to GitHub.
* `git branch -M main` - Renamed the default branch to main.
* `git push -u origin main` - Pushed the initial code to the remote server.

### 3. Creating Commit History
* `echo 'print("commit 1")' >> code.py && git commit -a -m "commit 1"`
* `echo 'print("commit 2")' >> code.py && git commit -a -m "commit 2"`
* `echo 'print("commit 3")' >> code.py && git commit -a -m "commit 3"`
* `echo 'print("commit 4")' >> code.py && git commit -a -m "commit 4"`

### 4. Modifying History (Reset & Amend)
* `git reset --soft HEAD^^` - Deleted the last two commits but kept the code changes staged.
* `git commit -m "commit after deletion"` - Created a new commit for the recovered changes.
* `echo 'print("finish")' >> code.py` - Added the final required line.
* `git add code.py`
* `git commit --amend -m "finish"` - Merged the new change into the last commit and renamed it.

### 5. Bonus: Revert (Undo without Deleting)
* `git revert HEAD~3..HEAD` - Reverted the changes from 3 commits back.
* (Inside Vim): Changed the message to `"after revert"`.
* `git push origin main --force` - Force pushed the modified history to GitHub.

