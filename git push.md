#git #command
`git push` is a Git command that uploads your local commits to a remote repository, updating the remote branch.

- Sends your changes from a local branch to a matching remote branch.
- Commonly used to share your work with others
- The remote branch is updated first
- Then, Git automatically updates your local origin/main to reflect the new remote state (only  if the push successful)
- Git may reject the push if the remote has changes that you don't have locally - in that case, need to [[git pull]] first.