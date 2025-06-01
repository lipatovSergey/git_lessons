#git #command
# Git — Tag

**Tags** are used to mark specific commits in a repository — typically for versioning or other important milestones (e.g., `v1.0.0`). This allows easier reference and access to specific states of the project.

---

## 🔖 Creating Tags

### ✅ Lightweight Tag

A simple pointer to a commit (no additional metadata):

```bash
git tag v1.0.0
```

### ✅ Annotated Tag

Recommended: contains metadata like author, date, and message:

```bash
git tag -a v1.0.0 -m "Release version 1.0.0"
```

---

## 📍 Where Is the Tag Placed?

- A tag is added to the **commit currently pointed to by `HEAD`**.
    
- Example:
    
    ```bash
    git tag v1
    ```
    
    This adds `v1` to the **last commit that was made**.
    
- You can also tag a **specific commit** by hash:
    
    ```bash
    git tag <tag-name> <commit-hash>
    ```
    
    You only need the first **7 characters** of the commit hash. You can find hashes using:
    
    ```bash
    git log
    ```
    

---

## 📋 Viewing Tags

To list all tags:

```bash
git tag
```

---

## 🗑 Deleting Tags

### Locally:

```bash
git tag -d <tag-name>
```

### Remotely:

```bash
git push origin --delete tag <tag-name>
```

---

## 📦 Pushing Tags to Remote

Tags **are not pushed automatically**. Push a single tag:

```bash
git push origin v1.0.0
```

Or push all local tags:

```bash
git push origin --tags
```

---

## 🔄 Using Tags

You can check out code at the point of a tag:

```bash
git checkout v1.0.0
```

This puts you in **detached HEAD** state — useful for exploring or testing that version.
[[git tag]]

[[git checkout]]

[[git log]]

[[Git main]]

[[git restore]]