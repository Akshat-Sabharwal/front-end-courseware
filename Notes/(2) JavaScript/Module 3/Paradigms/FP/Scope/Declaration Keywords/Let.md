It is generally used when *scoped to a block*.
### Properties
* It cannot be redeclared
```js
// Initial declaration
let name = "John";

// Declaring the same variable again
let name = "Mary";
```

* It can be updated 
```js
// Initial Declaration
let name = "John";

// Updating its value
name = "Mary";
```

* It cannot be used before its declaration
```js
// Using the variable
console.log(name);

// Declaring the variable
let name = "John";
```
