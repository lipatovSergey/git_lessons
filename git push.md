#git #command
`git push` is a Git command that uploads your local commits to a remote repository, updating the remote branch.

- Sends your changes from a local branch to a matching remote branch.
- Commonly used to share your work with others
- The remote branch is updated first
- Then, Git automatically updates your local origin/main to reflect the new remote state (only  if the push successful)
- Git may reject the push if the remote has changes that you don't have locally - in that case, need to [[git pull]] first.

## git push [[Tracking Relationship Between Local and Remote Branches]]

### By default git push:
- checks which remote branch the current local branch is tracking
- then pushes your commits into that specific remote branch
- Example: `git push` pushes from the current branch (e.g. main) to its tracking branch (e.g. origin/main)
### We use `git push <remote> <place>`.
- This overrides the default behavior 
- You explicitly say "Push commits from this branch to that branch on this remote"
- Works even if you are not currently checked out on that branch
- Git push to the remote branch with the same name
- Tracking configuration is ignored
- If the remote branch doesn't exist, git will create it automatically
	- You can also set up tracking on this branch after pushing by using:  `git push -u origin my-feature`. This means future [[git pull]] or [[git push]] on my-feature will automatically use origin/my-feature. With out `-u` tracking wouldn't set automatically.