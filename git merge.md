#git #command
Used to merge changes from one branch to another. 
First example:
We have two branches `main` and `second`. In both were made changes since C1.
![[Pasted image 20250604184425.png]]
Now we want to continue our work in main branch, but we want to get code from `second` to continue. We run `git merge second`. And that's what we got
![[Pasted image 20250604184724.png]]
Git created new merge commit C7, which combines the changes from both `main` and `second` branches.

# Fast-forward

For example our repo looks like this
![[Pasted image 20250604185109.png]]
We finished working on `second`. And now we want to add it to main. We run `git merge second` while we at the main branch. 
That what we got 
![[Pasted image 20250604185351.png]]
Because there were no changes in `main` while we worked at `second` branch. Git performed a fast-forward merge and moved the `main` branch pointer to match the `second`.