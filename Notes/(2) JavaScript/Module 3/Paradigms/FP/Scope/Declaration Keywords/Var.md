The `var` keyword is the most lenient one.

### Properties
* It can be redeclared
```js
// Initial declaration
var name = "John";

// Declaring the same variable again
var name = "Mary";
```

* It can be updated 
```js
// Initial Declaration
var name = "John";

// Updating its value
name = "Mary";
```

* It can be used even before its declaration
```js
// Using the variable
console.log(name);

// Declaring the variable
var name = "John";
```
