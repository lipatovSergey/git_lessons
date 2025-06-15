#git #command  
`git pull` is a Git command that downloads changes from a remote repository and immediately merges them into your current local branch.

---

### 🔁 It's a shortcut for:

```bash
git fetch
git merge origin/your-branch
```

- It updates your files and commits with new changes from the remote.
    
- Can cause **merge conflicts** if both you and someone else changed the same part of the code.
    
- Commonly used to **stay up to date** with the remote repository.
    

---

### 🔄 `git pull --rebase` is a shortcut for:

```bash
git fetch
git rebase origin/your-branch
```

- Rewrites your local commits as if they were made **after** the remote changes.
    
- Keeps history linear by avoiding merge commits.
    

---

###  Pulling with arguments:

- You can specify:
    
    ```bash
    git pull origin branch-name
    ```
    
    → This is equal to:
    
    ```bash
    git fetch origin branch-name
    git merge origin/branch-name
    ```
    
- You can also use **colon refspecs**:
    
    ```bash
    git pull origin source:destination
    ```
    
    → Git fetches `source` from the remote and puts it into local `destination`, then merges `destination` into your current branch.
    
    Example:
    
    ```bash
    git pull origin main:foo
    ```
    
    - Fetches `origin/main` into a new local branch `foo`
        
    - Then merges `foo` into the current branch
        

---

###  Pulling with empty source (rare case):

```bash
git pull origin :foo
```

- Creates a **new empty local branch `foo`**
    
- Attempts to merge it into the current branch (if valid)
    
- This behavior mirrors `git fetch` with an empty source and is rarely used in practice

