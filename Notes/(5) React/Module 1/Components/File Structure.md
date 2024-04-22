The component file which contains the component is written in a mix of JavaScript and other languages called [[JSX]].

Components in React are broadly of two types. 
* **Functional Components** → More commonly used  
* **Class Components** → Not-so commonly used

### Functional Components
It basically means ***components that are in the form of functions***.

##### Concept
In JavaScript, **functions** are created to be used whenever needed. 
For instance, to log a greeting for a few people in the console, a better way than this,
```js
console.log("Hello, John!");
console.log("How are you?");

console.log("Hello, Mary!");
console.log("How are you?");

console.log("Hello, Isiaha!");
console.log("How are you?");

console.log("Hello, Kumar!");
console.log("How are you?");
```

would be to declare a function and call it.
```js
function greet(name) {
	console.log(`Hello ${name}!`);
	console.log("How are you?");
}

greet(John);
greet(Mary);
greet(Isiaha);
greet(Kumar);
```

Similarly, components can be created in the form of functions. So that they can be used whenever needed.

##### Syntax
It is much like declaring a JavaScript function.
```jsx
function ComponentName() {
	return (
	 <!-- HTML code here -->
	)
}
```

| Code | What it means |
|--|--|
| `function` | The keyword to denote a functional component |
| `ComponentName` | The name of the component should always be in CamelCase |
| `return()` | This tells the compiler to display the code, given here, on the webpage |

##### Example
In order to create a basic React component named `Heading`,
```jsx
// Heading.js

// Name in CamelCase
function Heading() {

	// If the HTML code is in one-line, brackets can be omitted
	return <h1>Hello World!</h1>;
}
```

### Export Statement
These components need to be accessed by the **root component**, or *the first container of the file*, of the React app. 

For this, the component needs to be ***exported*** or *make it available for the app to use from another file*.
```jsx
export { Heading };
```

For multiple components or any JavaScript component like variables, functions, object,
```js
export { name1, getName, Heading };
```
