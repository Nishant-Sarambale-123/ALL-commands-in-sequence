Here’s a **complete Git command flow (step-by-step)** from starting → working → pushing → advanced usage. This is structured exactly how you’d use Git in real projects 👇

---

# 🚀 1. Initial Git Setup (First Time Only)

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --list
```

👉 Optional:

```bash
git config --global init.defaultBranch main
```

---

# 📁 2. Start a Repository

### Create new repo

```bash
git init
```

### Or clone existing repo

```bash
git clone <repo-url>
cd <repo-folder>
```

---

# 📌 3. Check Status

```bash
git status
```

---

# ➕ 4. Add Files (Staging)

### Add single file

```bash
git add file.txt
```

### Add all files

```bash
git add .
```

---

# 💾 5. Commit Changes

```bash
git commit -m "Initial commit"
```

---

# 🔄 6. Connect to Remote Repository

```bash
git remote add origin <repo-url>
git remote -v
```

---

# ⬆️ 7. Push Code to Remote

### First push

```bash
git push -u origin main
```

### Next pushes

```bash
git push
```

---

# ⬇️ 8. Pull Latest Changes

```bash
git pull origin main
```

---

# 🌿 9. Branching (Very Important)

### Create branch

```bash
git branch feature-branch
```

### Switch branch

```bash
git checkout feature-branch
```

👉 New way:

```bash
git switch feature-branch
```

### Create + switch

```bash
git checkout -b feature-branch
```

---

# 🔀 10. Merge Branch

```bash
git checkout main
git merge feature-branch
```

---

# ❌ 11. Delete Branch

```bash
git branch -d feature-branch
```

---

# 🔍 12. View History

```bash
git log
git log --oneline
```

---

# 🧾 13. See Changes

```bash
git diff
git diff --staged
```

---

# ♻️ 14. Undo Changes

### Unstage file

```bash
git restore --staged file.txt
```

### Discard changes

```bash
git restore file.txt
```

### Undo last commit (keep changes)

```bash
git reset --soft HEAD~1
```

### Undo commit completely

```bash
git reset --hard HEAD~1
```

---

# 🔁 15. Stash (Temporary Save)

```bash
git stash
git stash list
git stash apply
git stash pop
```

---

# 🔗 16. Work with Remote

```bash
git fetch
git pull
git push
```

---

# 🏷️ 17. Tagging

```bash
git tag v1.0
git push origin v1.0
```

---

# 🔐 18. Remove Remote

```bash
git remote remove origin
```

---

# 🧹 19. Clean Untracked Files

```bash
git clean -f
```

---

# 📦 20. Advanced Useful Commands

### Rebase

```bash
git rebase main
```

### Cherry-pick

```bash
git cherry-pick <commit-id>
```

### Show commit

```bash
git show <commit-id>
```

---

# 🧠 Real DevOps Workflow (Most Important)

```bash
git clone <repo>
cd project
git checkout -b feature
# do changes
git add .
git commit -m "feature added"
git push origin feature
# create PR → merge
git pull origin main
```

---

# ✅ Key Takeaway

👉 Git flow always follows this pattern:

```
init/clone → add → commit → push → pull → branch → merge
```

---

If you want, I can also give:
✅ Interview questions on Git
✅ Real DevOps scenarios (merge conflict, rebase vs merge)
✅ Cheat sheet PDF

Just tell 👍
