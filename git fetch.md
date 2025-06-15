#git #command
`git fetch` is a Git command that downloads new commits from remote repository but doesn't change your local branches or files.

- It updates remote tracking branches like [[origin main]], origin dev, etc.
- Your local branches stay the same - no merges, no file changes.
- It's like taking a snapshot of the remote repo to see what has changed.
- Useful for reviewing others work before merging or pulling.

### `git fetch <remote> <branch>`
- Downloads commits from the remote `<branch>` and updates `origin/<branch>` locally.
- Does not update your local `<branch>` even if it has the same name.

### `git fetch <remote> <source>:<destination>`
- Downloads commits from remote `<source>` and writes them into local `<destination>`
- Example: `git fetch origin feature:new-feature`. Fetches origin/feature and writes it to local new-feature branch.
- <font color="#c00000">⚠️ </font> Git won't allow fetching into a branch that is currently checked out.
- If the `<destination>` doesn't exist, git will create the local branch automatically and write the commits into it.
- Git allows to specify "nothing" as `<source>` `git fetch origin :branch-name` 
	- Creates a new local branch named branch-name that points to nothing (usually FETCH_HEAD)
	- You can later assign or reset it