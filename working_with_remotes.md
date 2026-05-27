# Module 03 – Working with Remotes

## Git Commands Used

---

# Clone Repositories

```bash
git clone https://github.com/user/repo.git
```

```bash
cd repo && ls
```

```bash
git clone https://github.com/user/repo.git my-project
```

---

# Managing Remotes

```bash
git remote add origin https://github.com/user/repo.git
```

```bash
git remote -v
```

```bash
git remote set-url origin git@github.com:user/repo.git
```

```bash
git remote remove origin
```

---

# Push Commands

```bash
git push
```

```bash
git push origin main
```

```bash
git push -u origin main
```

```bash
git push --force
```

---

# Pull Commands

```bash
git pull
```

```bash
git pull origin main
```

```bash
git pull --rebase
```

```bash
git pull --ff-only
```

---

# Fetch Commands

```bash
git fetch
```

```bash
git log origin/main
```

---

# Origin & Upstream

```bash
git push origin main
```

```bash
git pull upstream main
```

---

# Daily Workflow Commands

## Pull latest changes

```bash
git pull origin main
```

## Check status

```bash
git status
```

## Stage changes

```bash
git add .
```

## Commit changes

```bash
git commit -m "feat: add new feature"
```

## Pull with rebase

```bash
git pull --rebase origin main
```

## Push to remote

```bash
git push origin main
```
