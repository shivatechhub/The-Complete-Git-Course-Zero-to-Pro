# Module 07 – Intermediate Git Tools Commands

## git diff

### Show unstaged changes
```bash
git diff
```

### Show staged changes
```bash
git diff --staged
```

### Compare all changes against last commit
```bash
git diff HEAD
```

### Compare two branches
```bash
git diff main..feature - for explaining git
```

### Compare last 3 commits
```bash
git diff HEAD~3 HEAD
```

### Show summary only
```bash
git diff --stat
```

### Compare last commit changes with statistics
```bash
git diff HEAD~1 HEAD --stat
```

---

# git blame

### Show line-by-line author information
```bash
git blame auth.js
```

### Show blame for specific line range
```bash
git blame -L 10,20 auth.js
```

### Ignore whitespace changes
```bash
git blame -w auth.js
```

### Blame specific section of file
```bash
git blame -L 10,25 auth.js
```

---

# git bisect

### Start bisect session
```bash
git bisect start
```

### Mark current commit as bad
```bash
git bisect bad
```

### Mark known good commit
```bash
git bisect good <hash>
```

### Mark current commit as good
```bash
git bisect good
```

### Reset bisect session
```bash
git bisect reset
```

### Automatically run tests during bisect
```bash
git bisect run npm test
```

### Example workflow
```bash
git bisect start
git bisect bad
git bisect good a3f1c2b
git bisect bad
git bisect good
git bisect bad
git bisect reset
```

---

# git cherry-pick

### Cherry-pick a single commit
```bash
git cherry-pick <hash>
```

### Cherry-pick multiple commits
```bash
git cherry-pick <hash1> <hash2>
```

### Cherry-pick a commit range
```bash
git cherry-pick A..B
```

### Apply fix to another branch
```bash
git switch hotfix
git cherry-pick <fix-hash>
```

---

# git tag

### List tags
```bash
git tag
```

### Create lightweight tag
```bash
git tag v1.2.0
```

### Create annotated tag
```bash
git tag -a v1.2.0 -m "Release v1.2.0"
```

### Tag an older commit
```bash
git tag -a v1.0.0 9d4e8a1
```

### Push all tags
```bash
git push origin --tags
```

### Push a specific tag
```bash
git push origin <tag-name>
```

---

# Git Aliases

### General Syntax
```bash
git config --global alias.<short> "<full-command>"
```

### Checkout Alias
```bash
git config --global alias.co "checkout"
git co main
```

### Common Aliases

```bash
git config --global alias.co "checkout"
git config --global alias.br "branch"
git config --global alias.st "status"
git config --global alias.cm "commit -m"
git config --global alias.lg "log --oneline --graph --all"
git config --global alias.undo "reset --soft HEAD~1"
git config --global alias.amend "commit --amend --no-edit"
git config --global alias.unstage "restore --staged"
```

---

# Real-World Debugging Workflow

### 1. Check what changed
```bash
git diff HEAD~1 HEAD --stat
```

### 2. Check who modified code
```bash
git blame -L 10,25 auth.js
```

### 3. Find the bad commit
```bash
git bisect start
git bisect bad
git bisect good v1.2.0
```

### 4. Apply fix to another branch
```bash
git switch hotfix
git cherry-pick <fix-hash>
```

---

# Pro Habits Commands

### Review staged changes before commit
```bash
git diff --staged
```

### Ignore whitespace when blaming
```bash
git blame -w <file>
```

### Automate bisect testing
```bash
git bisect run <test-command>
```

### Cherry-pick urgent fixes
```bash
git cherry-pick <hash>
```

### Tag releases
```bash
git tag -a v2.0.0 -m "Release v2.0.0"
```

### Push tags explicitly
```bash
git push origin --tags
```

### Create useful aliases
```bash
git config --global alias.lg "log --oneline --graph --all"
```

### View statistics summary
```bash
git log --stat
git diff --stat
```