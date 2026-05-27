# The Complete Git Course: Zero to Pro
GIT is version control tool that provides a set of commands to manage the source code. 
some operations involve. 
```
  * cloning the existing repo
  * creating a new branch
  * commiting the code.
  * pull/fetch the code from the remote branch.
  * push the code.
  * resolving the merge conflicts.
  * rebase the code. 
```

## Basic GIT Commands <br>

1. git init: Initializes a new Git repository in the current 
directory. <br>
```
$ git init
```

2. git clone: Clones a repository from a remote 
URL to your local machine. <br>
```
$ git clone <repo_url>
```

3. git status: Shows the working directory status (which files are 
modified, staged, etc.). <br>
```
$ git status
```
4. git add : Stages a file or files to be committed. <br>
```
$ git add *
$ git add filename1 filename2
```

5. git commit -m "message": Commits staged changes to the 
local repository with a message. <br>
```
$ git commit -m "sample commit message"
```

6. git push: Pushes committed changes to the remote repository. <br>
```
$ git push origin main
$ git push origin <branch_name>
$ git push
```

7. git pull: Fetches and merges changes from the remote <br>
repository to your local working directory. <br>
```
$ git pull origin main
$ git pull origin <branch_name>
$ git pull
```

8. git fetch: Downloads objects and refs from another repository 
(without merging). <br>
```
$ git fetch origin main
$ git fetch origin <branch_name>
$ git fetch --all
```

9. git merge : Merges changes from the specified branch into the 
current branch. <br>
```
$ git merge origin main
$ git merge <feature_branch>
```

10. git log: Shows the commit history of the repository. <br>
```
$ git log
$ git log -n 5 (shows last 5 commits)
$ git log feature-branch (commit history for specific feature branch)
$ git log --oneline (for compact view)
$ git log --oneline -n 5 (shows last 5 commits in oneline)
$ git log --author="Alice" (commits by a specific Author)
$ git log --since="2025-01-01" (commits from the Date)
$ git log --until="2025-02-01" (commits before a specific date)
```

11. git diff: Shows the differences between your working 
directory and the index (staged changes). <br>
```
$ git diff
$ git diff --staged (difference between staged changes and last commit) 
$ git diff <commit1> <commit2> (difference between 2 commits)
$ git diff main..feature-branch (difference between main branch and Feature branch)
$ git diff path/to/file.txt (shows changes made to a specific file)
$ git diff --word-diff (shows the word by word differences)
$ git diff --stat (to show the summary of changes)
```



## Branching Commands
1. git branch: Lists all branches in your repository. <br>
```
$ git branch
```
2. git branch <branch_name>: Creates a new branch. <br>
```
$ git branch feature-branch
```
3. git checkout <branch_name>: Switches to an existing 
branch. <br>
```
git checkout feature-branch
```
4. git checkout -b <branch_name>: Creates and switches to a 
new branch in one step. <br>
```
git checkout feature-branch
git checkout -b new-feature
```
5. git merge <branch_name>: Merges changes from the 
specified branch into the current branch.  <br>
```
$ git merge feature-branch
```
6. git rebase <branch_name>: Applies changes from one 
branch onto another branch (instead of merging). <br>
```
$ git rebase feature-branch
```
7. git branch -d <branch_name>: Deletes the specified branch 
(locally). <br>
```
$ git branch -d feature-branch
```
8. git branch -D <branch_name>: Forcefully deletes a branch 
(locally). <br>
```
$ git branch -D feature-branch
```
9. git remote set-head origin <branch_name>: Sets the 
default branch for the remote repository. <br>
```
$ git remote set-head origin feature-branch
```

##  Remote Commands (Managing remotes and syncing with the cloud) 
1. git remote -v: Shows the remote repository URLs. 
```
$ git remote -v
```
2. git remote add : Adds a new remote repository. 
```
$ git remote add origin https://github.com/username/repository.git
```
3. git remote remove : Removes a remote repository. 
```
$ git remote remove origin
```
4. git push origin <branch_name>: Pushes a branch to a remote repository. 
```
$ git push origin feature-branch
```
5. git push -u origin <branch_name>: Pushes a branch to a remote repository and sets the upstream for the branch. 
```
$ git push -u origin feature-branch
```
6. git pull origin <branch_name>: Fetches and merges a branch from the remote repository. 
```
$ git pull origin feature-branch
```
7. git fetch origin: Downloads objects and refs from the remote repository. 
```
$ git fetch origin
```
8. git remote show origin: Displays detailed information about a remote repository.
```
$ git remote show origin
```

## Staging and Committing (Managing changes) 

1. git add .: Stages all modified files in the working directory.
This command stages all the changes in your working directory, including modified and newly created files (but not deleted files).
```
$ git add .
$ git add -A  (This stages all changes, including deleted files.)
```

2. git reset: Unstages a file (reverts it to the working directory).
This command unstages a file, i.e., it removes it from the staging area but leaves the changes in the working directory.
```
$ git reset file.txt
```

3. git commit --amend: Modifies the last commit (can change the commit message or add changes).
This command allows you to amend the most recent commit. You can use it to change the commit message or add new changes to the commit.
Important: You can only amend the last commit in your local repository (before it has been pushed to a remote).
```
$ git commit --amend -m "Updated commit message"
```

4. git commit --all: Automatically stages tracked files and commits them.
This command automatically stages all modified and deleted files that are already tracked (i.e., files that have been previously added to Git). It then commits them in one step.
```
$ git commit --all -m "Commit all tracked changes"
```

5. git commit -a: Stages and commits all modified files.
This is shorthand for git commit --all. It stages all modified and deleted tracked files and commits them in one step.
```
$ git commit -a -m "Staging and committing all modified files"
```

6. git commit --no-verify: Skips pre-commit hooks while committing.
This command skips the execution of pre-commit hooks, which are typically used to run tests, linters, or other checks before committing. Use this if you want to bypass those checks.
```
$ git commit --no-verify -m "Commit without pre-commit hooks"
```

7. git reset --soft HEAD~1: Moves the HEAD pointer back one commit but leaves your changes staged.
This command moves the HEAD pointer (and the current branch) back by one commit, but it keeps the changes you made in the working directory and staged. This is useful if you want to edit the last commit or amend it.
```
$ git reset --soft HEAD~1
```

8. git reset --hard HEAD~1: Moves the HEAD pointer back one commit and discards changes in the working directory.
This command resets the HEAD pointer back by one commit, and discards all changes in the working directory and the staging area. This is a destructive operation as it permanently removes uncommitted changes.
```
$ git reset --hard HEAD~1
```

## Viewing and Comparing Changes (Inspecting changes) 
| Command                                 | Description                                                             | Example Command                                  |
|-----------------------------------------|-------------------------------------------------------------------------|-------------------------------------------------|
| **`git diff`**                          | Shows changes between your working directory and the index (unstaged changes). | `git diff`                                      |
| **`git diff --staged`**                 | Shows changes between the staged files and the last commit.              | `git diff --staged`                             |
| **`git diff <commit_id>`**              | Shows the differences between the working directory and a specific commit. | `git diff abc1234`                              |
| **`git log`**                           | Displays the commit history.                                             | `git log`                                       |
| **`git log --oneline`**                 | Displays the commit history in a simplified one-line format.             | `git log --oneline`                             |
| **`git log --graph`**                   | Displays the commit history as a graph.                                  | `git log --graph`                               |
| **`git log --author="name"`**           | Filters commits by a specific author.                                    | `git log --author="John Doe"`                   |
| **`git log --since="2 weeks ago"`**     | Filters commits made after a specific date.                              | `git log --since="2 weeks ago"`                 |
| **`git blame <file_path>`**             | Shows line-by-line annotations for a file, telling who last modified each line. | `git blame README.md`                          |
| **`git show <commit_id>`**              | Shows details of a specific commit, including diff and metadata.        | `git show abc1234`                              |
| **`git show <commit_id>:<file_path>`**  | Shows a specific file at a particular commit along with the diff.        | `git show abc1234:README.md`                    |

## Reverting and Resetting (Undoing changes)
| Command                                      | Description                                                                 | Example Command                                          |
|----------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------|
| **`git reset <commit_id>`**                  | Moves HEAD to a specific commit, leaving your working directory intact.     | `git reset abc1234`                                      |
| **`git reset --hard <commit_id>`**           | Resets your working directory, index, and HEAD to a specific commit (all changes will be lost). | `git reset --hard abc1234`                               |
| **`git reset --soft <commit_id>`**           | Resets only the HEAD to a specific commit, leaving staged changes.         | `git reset --soft abc1234`                               |
| **`git reset --mixed <commit_id>`**          | Resets the HEAD and index to a specific commit but keeps the working directory unchanged. | `git reset --mixed abc1234`                              |
| **`git revert <commit_id>`**                 | Creates a new commit that undoes the changes of the specified commit.      | `git revert abc1234`                                     |
| **`git restore <file_path>`**                | Restores the file(s) in the working directory from the index or a commit.  | `git restore README.md`                                  |
| **`git restore --staged <file_path>`**       | Removes a file from the staging area.                                       | `git restore --staged README.md`                         |
| **`git clean -f`**                           | Removes untracked files in the working directory.                          | `git clean -f`                                           |
| **`git clean -fd`**                          | Removes untracked files and directories.                                   | `git clean -fd`                                          |

## Stashing (Temporarily saving changes)
| Command                                      | Description                                                                 | Example Command                                            |
|----------------------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------|
| **`git stash`**                              | Stashes the changes in your working directory (both staged and unstaged).   | `git stash`                                                |
| **`git stash list`**                         | Lists all the stashes.                                                     | `git stash list`                                           |
| **`git stash pop`**                          | Applies the latest stash and removes it from the stash list.                 | `git stash pop`                                            |
| **`git stash apply`**                        | Applies a stash without removing it from the list.                           | `git stash apply`                                          |
| **`git stash drop`**                         | Removes a specific stash from the stash list.                               | `git stash drop stash@{0}`                                 |
| **`git stash clear`**                        | Clears all stashes.                                                        | `git stash clear`                                          |
| **`git stash save "message"`**               | Stashes changes with an optional message for identification.                | `git stash save "WIP changes"`                              |
| **`git stash branch <branch_name>`**         | Creates a new branch from the stash and applies it.                         | `git stash branch my-feature-branch`                       |

##  Tags (Managing versions) 
| Command                                      | Description                                                                 | Example Command                                             |
|----------------------------------------------|-----------------------------------------------------------------------------|------------------------------------------------------------|
| **`git tag`**                                | Lists all tags in the repository.                                           | `git tag`                                                   |
| **`git tag <tag_name>`**                     | Creates a new tag at the current commit.                                    | `git tag v1.0`                                              |
| **`git tag -a <tag_name> -m "message"`**      | Creates an annotated tag with a message.                                    | `git tag -a v1.0 -m "Initial release"`                       |
| **`git tag -d <tag_name>`**                   | Deletes a tag locally.                                                     | `git tag -d v1.0`                                            |
| **`git push origin <tag_name>`**              | Pushes a specific tag to the remote repository.                             | `git push origin v1.0`                                       |
| **`git push origin --tags`**                  | Pushes all tags to the remote repository.                                   | `git push origin --tags`                                     |
| **`git fetch --tags`**                        | Fetches all tags from the remote repository.                               | `git fetch --tags`                                           |

##  Git Config and Info (Configuration and repository information)
| Command                                           | Description                                                                 | Example Command                                                 |
|---------------------------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------|
| **`git config --global user.name "Your Name"`**    | Sets your global username for commits.                                      | `git config --global user.name "John Doe"`                       |
| **`git config --global user.email "youremail@example.com"`** | Sets your global email for commits.                                         | `git config --global user.email "john.doe@example.com"`          |
| **`git config --list`**                           | Lists all configuration settings.                                           | `git config --list`                                              |
| **`git config <key> <value>`**                    | Sets a specific configuration option.                                       | `git config core.editor "vim"`                                   |
| **`git config --global core.editor <editor>`**    | Sets the default text editor for Git.                                       | `git config --global core.editor "vim"`                          |
| **`git config --global color.ui true`**           | Enables colored output in Git.                                             | `git config --global color.ui true`                               |
| **`git config --global alias.st status`**         | Creates a custom Git alias (e.g., `git st` for `git status`).               | `git config --global alias.st status`                            |

## Git Hooks (Automated scripts triggered by Git actions)
| Command                                             | Description                                                                 | Example Command                                                |
|-----------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------------|
| **`git init`**                                      | Creates a `.git/hooks` directory, where hook scripts are stored.            | `git init`                                                     |
| **`git commit-msg`**                                | A hook that runs before a commit message is saved (can enforce message formats). | `git commit-msg`                                               |
| **`git pre-commit`**                                | A hook that runs before a commit is made (can be used for checks like linting). | `git pre-commit`                                               |
| **`git post-commit`**                               | A hook that runs after a commit is made.                                    | `git post-commit`                                              |

## Git Submodules (Managing external repositories within a project)
| Command                                                   | Description                                                                 | Example Command                                                 |
|-----------------------------------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------|
| **`git submodule add <repo_url>`**                         | Adds a new submodule to the repository (downloads an external repo).        | `git submodule add https://github.com/example/repo.git`          |
| **`git submodule init`**                                   | Initializes the submodules configured in the repository (after cloning).    | `git submodule init`                                            |
| **`git submodule update`**                                 | Updates the submodules to the commit specified in the superproject.         | `git submodule update`                                          |
| **`git submodule status`**                                 | Displays the current commit of the submodule.                               | `git submodule status`                                          |
| **`git submodule deinit <submodule_path>`**                | Removes a submodule from the working directory.                             | `git submodule deinit path/to/submodule`                         |
| **`git submodule update --remote`**                        | Updates the submodule to the latest commit from the remote repository.     | `git submodule update --remote`                                  |
| **`git submodule foreach <command>`**                      | Runs a command in each submodule.                                          | `git submodule foreach 'git pull origin main'`                   |

## Git Workflow Commands (Working with others and managing collaboration)
| Command                                                   | Description                                                                 | Example Command                                                |
|-----------------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------------|
| **`git pull --rebase`**                                   | Fetches and applies remote changes, rebasing your local commits on top of them. | `git pull --rebase`                                            |
| **`git rebase -i <commit_id>`**                           | Starts an interactive rebase to modify commit history (e.g., squash, reword commits). | `git rebase -i HEAD~3`                                         |
| **`git rebase --continue`**                               | Continues the rebase after resolving conflicts.                             | `git rebase --continue`                                        |
| **`git rebase --abort`**                                  | Aborts the rebase process and restores the original state.                  | `git rebase --abort`                                           |
| **`git merge --no-ff`**                                   | Merges a branch with a "no fast-forward" option to ensure a merge commit is created. | `git merge --no-ff feature-branch`                             |
| **`git pull --no-commit`**                                | Pulls changes but doesn't automatically commit them.                        | `git pull --no-commit`                                         |
| **`git push --force-with-lease`**                          | Forces a push but checks if the remote branch has been updated (safer than `git push --force`). | `git push --force-with-lease`                            |
| **`git push --force`**                                     | Forces a push to the remote branch, potentially overwriting changes.       | `git push --force`                                             |
| **`git cherry-pick <commit_id>`**                          | Applies the changes from a specific commit onto the current branch.        | `git cherry-pick abc1234`                                      |

## Git Merge Strategies (Handling merge conflicts and strategies) 
| Command                                                        | Description                                                                 | Example Command                                                 |
|----------------------------------------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------|
| **`git merge --strategy=ours <branch_name>`**                   | Resolves merge conflicts by favoring the current branch’s changes.          | `git merge --strategy=ours feature-branch`                      |
| **`git merge --strategy=theirs <branch_name>`**                 | Resolves merge conflicts by favoring the other branch’s changes.            | `git merge --strategy=theirs feature-branch`                    |
| **`git merge --abort`**                                         | Aborts the merge process if there are conflicts and restores the working directory. | `git merge --abort`                                             |

## Git bisect (Finding the commit that introduced a bug) 
| Command                                                | Description                                                              | Example Command                                                   |
|--------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| **`git bisect start`**                                  | Starts a binary search for the commit that introduced a bug.             | `git bisect start`                                                |
| **`git bisect bad`**                                    | Marks the current commit as "bad" (where the bug is present).            | `git bisect bad`                                                  |
| **`git bisect good <commit_id>`**                       | Marks a commit as "good" (where the bug was not present).                | `git bisect good abc1234`                                         |
| **`git bisect reset`**                                  | Ends the bisect process and restores the repository to the state it was before starting the bisect. | `git bisect reset`                                      |
| **`git bisect log`**                                    | Displays the log of the bisect process.                                  | `git bisect log`                                                  |

##  Git Hooks for Automation (Pre-commit and post commit hooks)
| Command                                             | Description                                                                 | Example Command                                              |
|-----------------------------------------------------|-----------------------------------------------------------------------------|--------------------------------------------------------------|
| **`git commit-msg`**                                 | A hook script that runs before the commit message is finalized (you can use this to enforce rules, like requiring certain keywords). | `git commit-msg`          |
| **`git pre-commit`**                                 | A hook that can be used to run checks on files before the commit is finalized, such as linters or tests. | `git pre-commit`                                      |
| **`git post-commit`**                                | A hook that is triggered after a commit has been completed, useful for triggering actions like notifications or build processes. | `git post-commit`             |
| **`git pre-push`**                                   | A hook that runs before a push to the remote repository is initiated. | `git pre-push`                                               |
| **`git post-merge`**                                 | A hook that runs after a merge, ideal for cleanup or setup tasks.            | `git post-merge`                                             |

## Git Clean and Prune (Cleaning up untracked files and 
garbage collection) 
| Command                                      | Description                                                                 | Example Command                                              |
|----------------------------------------------|-----------------------------------------------------------------------------|--------------------------------------------------------------|
| **`git clean -n`**                           | Shows which untracked files would be removed, but doesn’t actually delete them. | `git clean -n`                                               |
| **`git clean -f`**                           | Removes untracked files from the working directory.                         | `git clean -f`                                               |
| **`git clean -fd`**                          | Removes untracked files and directories.                                    | `git clean -fd`                                              |
| **`git gc`**                                 | Runs garbage collection, cleaning up unnecessary files and optimizing the repository. | `git gc`                                                     |
| **`git prune`**                              | Removes objects that are no longer needed (generally used for cleaning up in repositories with lots of history). | `git prune`                                           |

## Git Archive (Creating a snapshot of the repository)
| Command                                                        | Description                                                                  | Example Command                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------------------|----------------------------------------------------------------------|
| **`git archive --format=tar --output=<output_file>.tar <branch_name>`** | Creates a tarball archive of the repository at a specific branch.             | `git archive --format=tar --output=repo-archive.tar main`     |
| **`git archive --format=zip --output=<output_file>.zip <branch_name>`** | Creates a zip archive of the repository at a specific branch.                 | `git archive --format=zip --output=repo-archive.zip main`    |

## Git Blame and Annotate (Tracing the history of file content)
| Command                                    | Description                                                               | Example Command                                            |
|--------------------------------------------|---------------------------------------------------------------------------|------------------------------------------------------------|
| **`git blame <file_path>`**                | Shows who last modified each line of a file and when.                     | `git blame README.md`                                      |
| **`git annotate <file_path>`**             | An alias for `git blame`, which displays commit information for each line of a file. | `git annotate README.md`                                   |

## Git Reflog (Tracking changes in the HEAD reference)
| Command                                                            | Description                                                                 | Example Command                                                 |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------|
| **`git reflog`**                                                   | Displays a log of all movements of the HEAD pointer (useful for tracking changes like reset and rebase operations). | `git reflog`                 |
| **`git reflog show`**                                              | Displays a detailed view of HEAD and the state of the repository.           | `git reflog show`                                              |
| **`git reflog expire --expire=now --all`**                          | Removes all reflog entries that have expired.                               | `git reflog expire --expire=now --all`                         |
| **`git reflog delete <ref_id>`**                                    | Deletes a specific reflog entry.                                           | `git reflog delete <ref_id>`                                   |





