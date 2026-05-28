# Commands Used in This Video – Module 05: Undoing Things

```bash
# Restore a file to last committed state
git restore README.md

# Unstage a file but keep changes
git restore --staged config.js

# Restore all unstaged changes
git restore .

# Restore file from a specific commit
git restore --source=HEAD~2 file.js

# Reset commit but keep changes staged
git reset --soft HEAD~1

# Reset commit and unstage changes
git reset --mixed HEAD~1

# Reset commit and delete all changes
git reset --hard HEAD~1

# View commit history
git log --oneline

# Revert a specific commit
git revert a3f1c2b

# Revert a range of commits
git revert HEAD~3..HEAD

# Revert without auto commit
git revert --no-commit a3f1c2b

# Save current work temporarily
git stash

# Save stash with a message
git stash push -m "WIP: login form"

# View all stashes
git stash list

# Restore latest stash and remove it
git stash pop

# Restore stash but keep it in stash list
git stash apply

# Delete a specific stash
git stash drop

# Delete all stashes
git stash clear

# View reflog history
git reflog

# Recover lost commit using reflog
git reset --hard HEAD@{2}

# Create recovery branch from lost commit
git branch recovered HEAD@{2}

# Switch branches
git switch other-branch

# Switch back to previous branch
git switch back-to-original

# Create branch from reflog hash
git branch recovered <hash>

# Amend last commit message
git commit --amend -m "new msg"

# Recover commits using reflog and branch
git reflog && git branch recovered <hash>

# Recover using reflog in one command
git reflog && git branch recovered HEAD@{2}
```
