# Module 06 - Collaboration Workflows

## Pull Request Workflow

### Update Main Branch

```bash
git switch main
git pull
```

### Create Feature Branch

```bash
git switch -c feature/add-search
```

### Stage and Commit Changes

```bash
git add .
git commit -m "feat: add search bar"
```

### Push Branch

```bash
git push -u origin feature/add-search
```

---

## Forking Workflow

### Clone Your Fork

```bash
git clone https://github.com/YOU/project.git
```

### Add Original Repository as Upstream

```bash
git remote add upstream https://github.com/team/project.git
```

---

## Complete Pull Request Workflow

```bash
# Start from updated main
git switch main && git pull

# Create feature branch
git switch -c feature/add-dark-mode

# Commit changes
git add .
git commit -m "feat: add dark mode toggle"

git add .
git commit -m "test: cover dark mode preference"

# Push branch
git push -u origin feature/add-dark-mode
```

---

## Handling Pull Request Feedback

### Commit Review Fixes

```bash
git add .
git commit -m "address review: fix edge case"
```

### Rebase With Latest Main

```bash
git fetch
git rebase origin/main
```

### Squash Multiple Commits

```bash
git rebase -i HEAD~5
```

---

## Daily Collaboration Commands

### Pull Latest Changes

```bash
git pull origin main
```

### Create a Feature Branch

```bash
git switch -c feature/clear-name
```

### Commit Changes

```bash
git commit -m "feat: one logical change"
```

### Push Changes

```bash
git push origin feature/clear-name
```

### Delete Merged Branch

```bash
git branch -d feature/clear-name
```

---

## Git Commands Cheat Sheet

```bash
git switch main
git pull

git switch -c <branch-name>

git add .
git commit -m "<message>"

git push -u origin <branch-name>

git clone <repository-url>

git remote add upstream <repository-url>

git fetch

git rebase origin/main

git rebase -i HEAD~5

git pull origin main

git push origin <branch-name>

git branch -d <branch-name>
```

---

## Pull Request Lifecycle

1. Update local main branch.
2. Create a feature branch.
3. Make changes and commit.
4. Push branch to remote repository.
5. Open Pull Request.
6. Request reviewers.
7. Address review feedback.
8. Rebase if needed.
9. Merge Pull Request.
10. Delete merged branch.

---

## Forking Workflow Lifecycle

1. Fork the repository on GitHub.
2. Clone your fork locally.
3. Add the original repository as upstream.
4. Create a feature branch.
5. Commit and push changes to your fork.
6. Open a Pull Request from your fork to the original repository.
7. Address review comments.
8. Merge after approval.
