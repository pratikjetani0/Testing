# Git Basic commands

---

# 🧰 Essential Git Commands 

## 📌 1. `git init` — Start a repo

Creates a new Git repository.

```bash
git init
```

👉 Use when starting a new project

---

## 📌 2. `git clone` — Copy a repo

Download an existing repository.

```bash
git clone https://github.com/user/repo.git
```

👉 Use when working on an existing project

---

## 📌 3. `git status` — Check changes

Shows what’s happening in your repo.

```bash
git status
```

👉 First command you should run if you’re confused

---

## 📌 4. `git add` — Stage changes

Prepares files for commit.

```bash
git add file.txt
git add .
```

👉 Moves changes to staging area

---

## 📌 5. `git commit` — Save changes

Creates a snapshot of staged changes.

```bash
git commit -m "Added login feature"
```

---

## 📌 6. `git log` — View history

Shows commit history.

```bash
git log
```

👉 Use `--oneline` for short view:

```bash
git log --oneline
```

---

## 📌 7. `git diff` — See changes

Compare changes in files.

```bash
git diff
```

👉 Shows what changed before committing

---

## 📌 8. `git branch` — Manage branches

```bash
git branch        # list branches
git branch feature1  # create branch
```

---

## 📌 9. `git checkout` — Switch branches

```bash
git checkout feature1
```

👉 New way (recommended):

```bash
git switch feature1
```

---

## 📌 10. `git merge` — Combine branches

```bash
git checkout main
git merge feature1
```

👉 Combines feature branch into main

---

## 📌 11. `git pull` — Get latest changes

```bash
git pull origin main
```

👉 Fetch + merge in one command

---

## 📌 12. `git push` — Upload changes

```bash
git push origin main
```

👉 Sends your commits to remote repo

---

# 🧠 Simple Workflow Example

```bash
git init
git add .
git commit -m "first commit"
git branch feature
git switch feature
# make changes
git add .
git commit -m "feature work"
git switch main
git merge feature
git push origin main
```

---

# ⚡ Pro Tip

If you remember just these 5, you're already productive:

- `git status`
- `git add`
- `git commit`
- `git pull`
- `git push`

---

# 🔁 `git rebase` — Basic Usage

## 📌 1. Update your branch with latest `main`

```bash
git checkout feature
git rebase main
```

👉 Takes your `feature` commits and puts them on top of `main`

---

## 📌 2. Rebase from remote branch

```bash
git fetch origin
git rebase origin/main
```

👉 Very common before pushing code

---

## 📌 3. Interactive rebase (clean commits)

```bash
git rebase -i HEAD~3
```

👉 Lets you:

- combine commits
- rename commit messages
- remove commits

---

## 📌 4. If conflict happens

```bash
git add .
git rebase --continue
```

👉 Or cancel:

```bash
git rebase --abort
```

---

# ⏪ `git reset` — Basic Usage

## 📌 1. Undo last commit (keep changes)

```bash
git reset --soft HEAD~1
```

---

## 📌 2. Undo last commit (unstage changes)

```bash
git reset HEAD~1
```

---

## 📌 3. Delete last commit completely

```bash
git reset --hard HEAD~1
```

⚠️ This removes code permanently

---

# ⚡ Super Short Difference

- **Rebase** → “move my commits”
- **Reset** → “undo my commits”

---

# 🚨 Golden Rule

- Use **rebase** → for clean history
- Use **reset** → for fixing mistakes
- Avoid both on shared branches unless you know what you're doing

---

