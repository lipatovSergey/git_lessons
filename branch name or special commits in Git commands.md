#git

Branches and commits are just references. That's why many Git commands accept both.
##  Examples of commands where you can use **either a branch or a commit**:

### 🔁 `git rebase`

```bash
git rebase main        # using a branch name
git rebase a1b2c3d     # using a specific commit
```

### 🔀 `git merge`

```bash
git merge feature      # merge a branch
git merge a1b2c3d      # merge a specific commit (less common)
```

### 🔙 `git reset`

```bash
git reset main
git reset a1b2c3d
```

### 📍 `git checkout`

```bash
git checkout feature
git checkout a1b2c3d   # temporarily switch to a commit (detached HEAD)
```

### 📌 `git cherry-pick`

```bash
git cherry-pick main
git cherry-pick a1b2c3d   # most often used this way
```

---

## ⚠️ Keep in mind:

- A **branch** is just a pointer to a **commit**.
    
- When you provide a branch name, Git will use the **latest commit** in that branch.
    
- When you provide a commit SHA, Git works **directly with that commit**, regardless of which branch it's on.

