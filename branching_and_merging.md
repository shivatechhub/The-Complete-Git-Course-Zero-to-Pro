# Module 04 – Branching & Merging local changes.
# Module 04 – Branching & Merging to Explain the merge conflict scenario

## Git Commands Used

---

# Branch Commands

```bash
git branch
```

```bash
git branch -a
```

```bash
git branch feature/login
```

```bash
git checkout -b feature/login
```

```bash
git switch feature/login
```

```bash
git branch -m new-name
```

```bash
git branch -d feature/login
```

```bash
git branch -D feature/login
```

---

# checkout vs switch

## Using checkout

```bash
git checkout main
```

```bash
git checkout -b new
```

```bash
git checkout file.js
```

```bash
git checkout abc123
```

---

## Using switch & restore

```bash
git switch main
```

```bash
git switch -c new
```

```bash
git restore file.js
```

```bash
git switch --detach abc123
```

---

# Fast-Forward Merge

```bash
git switch main
```

```bash
git merge feature
```

---

# 3-Way Merge

```bash
git switch main
```

```bash
git merge feature -m "Merge feature"
```

---

# Merge Conflict Resolution

## Stage resolved file

```bash
git add config.js
```

## Commit merge resolution

```bash
git commit
```

## Abort merge

```bash
git merge --abort
```

---

# Complete Branch Workflow

## Create and switch branch

```bash
git switch -c feature/dark-mode
```

## Stage and commit changes

```bash
git add . && git commit -m "feat: add dark mode toggle"
```

## Switch back to main

```bash
git switch main
```

## Merge feature branch

```bash
git merge feature/dark-mode
```

## Delete merged branch

```bash
git branch -d feature/dark-mode
```

---

# Daily Branching Workflow

## Update main branch

```bash
git switch main && git pull
```

## Create feature branch

```bash
git switch -c feature/your-task
```

## Commit changes

```bash
git add . && git commit -m "msg"
```

## Fetch and rebase

```bash
git fetch
git rebase main
```

## Switch to main

```bash
git switch main
```

## Merge branch

```bash
git merge feature/your-task
```

## Delete branch

```bash
git branch -d feature/your-task
```
