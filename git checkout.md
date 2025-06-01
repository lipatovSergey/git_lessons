#git #command
Once it was used to switch branches. Now `switch` command more relevant for this. But checkout still can be very useful.

## Check code during specific commit
We can use `git checkout <commit hash>`, to get old version of code. This command will set HEAD to commit, not to the branch.
Commit hash can be checked in [[git log]]. Seven first characters is enough for checkout command.
To get back to the latest version use `git checkout <branch name>`

