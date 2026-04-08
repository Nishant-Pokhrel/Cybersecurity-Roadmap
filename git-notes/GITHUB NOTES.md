# Git & GitHub Notes

## 🔹 1. What is Git?
Git is a distributed version control system used to track changes in files and manage project history.

## 🔹 2. What is GitHub?
GitHub is a cloud platform that hosts Git repositories and enables collaboration, sharing, and version control.

---

## 🔹 3. Core Concepts

- **Repository (Repo)** → Project folder tracked by Git  
- **Working Directory** → Where you edit files  
- **Staging Area** → Where files go after `git add`  
- **Commit** → Snapshot of staged changes  
- **Branch** → Independent version of the project  
- **Remote** → GitHub repository  

---

## 🔹 4. Basic Commands

```bash
git init
git status
git add .
git commit -m "message"
git log
````

---

## 🔹 5. Connect to GitHub

```bash
git remote add origin <repo-url>
git branch -M main
git push -u origin main
```

---

## 🔹 6. Real Workflow (IMPORTANT)

```bash
git pull origin main --rebase
# make changes
git add .
git commit -m "update"
git push origin main
```

---

## 🔹 7. Merge Conflict

### Why it happens:

When the same file is changed in two places.

### Example:

```
<<<<<<< HEAD
your code
=======
other code
>>>>>>> origin/main
```

### Fix Steps:

1. Open the file
2. Keep the correct content
3. Remove `<<<<<<< ======= >>>>>>>`
4. Run:

```bash
git add file
git rebase --continue
```

---

## 🔹 8. Branching

```bash
git branch
git checkout -b feature-name
git switch main
```

---

## 🔹 9. Undo / Recovery

```bash
git restore file
git reset --soft HEAD~1
git reset --hard HEAD~1
```

* `--soft` → keeps changes
* `--hard` → deletes changes permanently

---

## 🔹 10. Debugging Commands

```bash
git status
git log
git diff
```

---

## 🔹 11. Common Problems & Fixes

### Push Rejected

```bash
git pull origin main --rebase
git push origin main
```

---

### Merge Conflict

Fix manually → `git add` → `git rebase --continue`

---

### Undo Last Commit

```bash
git reset --soft HEAD~1
```

---

### Force Push (DANGEROUS)

```bash
git push --force
```


## 🔹 12. Best Practices

* Always pull before push
* Commit small changes
* Write clear commit messages
* Avoid working directly on `main`
* Use `.gitignore`
* Check `git status` frequently


##  Learning Goal
To master Git, GitHub, and version control as part of my cybersecurity journey.