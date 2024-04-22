Say, in [[Course/FrontEnd Dev/(2) JavaScript/Module 3/Paradigms/FP/Scope/Concept#^e7cb89|this]] case, two students of the same name *Harry Snyder* belong to each of the classes. For the teachers, it would be easy to address them since there is only one *Harry Snyder* in each class. But for the *Principal*, this would create confusion since both of them belong to the same school.  

### Example
Variables declared in a block of code are *scoped to that block*. Here, two variables of the same name co-exist only  because one of them is scoped to the `for` **block**.
```js
// Declaring a variable at global scope
let name = "Harry Snyder";

function getName(classRoom) {
		let name = "Harry Snyder";
		console.log(name + classRoom);
}

getName("A");
console.log(name);
```

> [!note]
> This only works with [[Let|let]] and [[Const|const]] declaration keywords.

