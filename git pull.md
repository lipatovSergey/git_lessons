#git #command
`git pull` is a Git command that downloads changes from a remote repository and immediately merges them into your current local branch. 

It's a shortcut for
```bash
git fetch
git merge origin/your-branch
```
 - It updates your files and commits with new changes from remote.
 - Can cause merge conflicts if both you and someone else changed the same part or the code
 - Commonly used to stay up to date with the remote repository.

It's also possible to use `git pull --rebase`, it's a shortcut for:
```bash 
git fetch 
git rebase origin/your-branch
```
