#git #command

Rewrites commit history by "moving" one set of commits on top of another.

For example:
While we were at commit C1 in our main branch, we found some bug, that needed to be fixed. We created new branch `bugFix` to work on it. While we were working on bug fix, rest of team edited code in main branch and added new commit to main.
![[Pasted image 20250604182534.png]]
After we fixed the bug. We wanted to add our code to main branch. But now main branch isn't the same as when we started to deal with bug. Because of this we want to `rebase`. 
We ran `git rebase main` while our HEAD on `bugFix` branch.
![[Pasted image 20250604182733.png]]
Now we can continue to work in our `bugFix` branch as if it was always based on C5.