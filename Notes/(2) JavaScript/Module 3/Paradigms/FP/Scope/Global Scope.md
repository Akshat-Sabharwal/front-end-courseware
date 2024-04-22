The *Principal* [[Course/FrontEnd Dev/(2) JavaScript/Module 3/Paradigms/FP/Scope/Concept#^e7cb89|here]] must keep a check on students of the all the classes. She, thus, belongs to the **global scope**.

Variables declared at the **global scope** can be accessed anywhere within the program.

```js
// Declaring a variable at the global scope
var name = "John"

// Defining a function using the variable declared above
function printName() {
	console.log(name);
}
```