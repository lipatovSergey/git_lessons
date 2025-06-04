#git #command
Used to create a new commit that undoes previous commit. Use `revert` to safely undo commits (changes) in public/shared branches.
After `revert` we write which commit we want to undo. And it creates new commit with undone changes. 
`git revert C2` will create new commit  `C2'` with undone changes from `C2`
How it works, example.

We have three commit `A -> B -> C`.
In `B` commit code looks like this:
```JS
console.log("World")
```
Commit `C` added line `console.log("Hello")`
```JS
console.log("World")
console.log("Hello")
```
We run `git revert C`
Git created new commit `D`. `A -> B -> C -> D`. In `D` all changes that were done in `C` will be deleted. 
In `D` code will be
```JS
console.log("World")
```
