Standing for **JavaScript XML**, JSX is an *extension* of the JavaScript language. Simply put, JSX is a combination of HTML and JavaScript. ^5b2a82

### Embedded Expressions
Since, JSX is combination of HTML and JavaScript, JavaScript code can be added inside an HTML element and *vice-versa*.

##### Syntax 
The JavaScript expression or code can be added inside *curly-braces*, `{}`.
```jsx
const name = "John";

const nameElement = (<h1>{ name }</h1>);
```

##### Example
In order to create an `<h1>` HTML element with the output of a JavaScript function, the following code will be used.
```jsx
function addNumbers(a, b) {
	return a + b;
}

const numberElement = (<h1>{ addNumbers(3, 7) }</h1>);
```

