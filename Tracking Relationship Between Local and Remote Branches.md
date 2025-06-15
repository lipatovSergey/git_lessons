#git 

# How it works by default 
- When you clone a repository using [[git clone]], Git:
	- Creates a remote-tracking branches (like origin/main)
	- Creates a local branch (main) that automatically tracks origin/main

# How to manually set or change tracking
- Set tracking on existing branch: `git branch -u origin/brach-name`
	- Full form `git branch --set-upstream-to=origin/branch-name`
- Create a new branch with tracking: `git checkout -b new-branch origin/main`
	- or `git swith -c new-branch --track origin/main`

# How to verify the tracking relationship
Use: `git branch -vv`. Will show which branches are tracking which remote ones.