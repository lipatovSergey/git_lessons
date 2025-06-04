#git #command
Used to apply the changes introduced by an existing commit onto our current branch, without merging or rebasing an entire branch.
For example we have main branch. And we want to work on different futures in separate branches. After futures are ready we want to add them to our main branch, but we want to save branches where we work on this futures.

Let's say main in at commit C1, and we created 3 branches:
![[Pasted image 20250604172606.png]]
For example in main (C1) our code 
```js
console.log("Version from C1")
```

We run `git cherry-pick C3`
Our repo looks like this
![[Pasted image 20250604173121.png]]
In C3 developer added `bugFix` function. And now our code in C3' looks like this:
```js
console.log("Version from C1")

function bugFix() {
	console.log("Bug fixed!")
}
```

Now we run `git cherry-pick C4`. In C5 code isn't tested yet. And we want to add to our main stable version from C4.
Our repo looks like this now
![[Pasted image 20250604173551.png]]
```js
console.log("Version from C1")

function bugFix() {
	console.log("Bug fixed!")
}

function sideFeature() {
	console.log("Side feature added")
}
```

`git cherry-pick C7`
![[Pasted image 20250604173844.png]]

```js
// app.js
console.log("Version from C1");

function fixBug() {
  console.log("Bug fixed!");
}

function sideFeature() {
  console.log("Side feature here");
}

function anotherFeature() {
  console.log("Another feature added");
}
```