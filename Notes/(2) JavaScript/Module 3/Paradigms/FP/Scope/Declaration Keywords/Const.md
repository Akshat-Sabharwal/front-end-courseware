Just like `let`, it also used to scope a variable to a block. It is the most strict keyword in JavaScript.
It is generally used when **a variable's value must or should not change** making it a **const**-ant.

* It cannot be redeclared
```js
// Initial declaration
const name = "John";

// Declaring the same variable again
const name = "Mary";
```

* It cannot be updated 
```js
// Initial Declaration
const name = "John";

// Updating its value
name = "Mary";
```

* It cannot be used before its declaration
```js
// Using the variable
console.log(name);

// Declaring the variable
const name = "John";
```
