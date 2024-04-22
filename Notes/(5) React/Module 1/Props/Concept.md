Now comes the task of adding the actual weather data in each card of the webpage and displaying the actual temperature on the webpage.

![[Pasted image 20231115181231.png|450]]

This can't be done using *static* or *still* HTML as the current temperature is not always the same. 
```html
<h1>26°C</h1>

<li>35°C</li>
```

There should be something like a variable which when updated would update the current temperature on the webpage, as well. 

**Props** are the solution, here.

### The What
In JavaScript, to pass data to a function, a parameter is added.
```js
function func(param) {
	console.log(param);
}
```

In React, ***Props*** or **Properties** play the same role as the parameter of a JavaScript function. 
```jsx
function Component(props) {
	return (
		<h1>{ props.attribute1 }</h1>
		<h2>{ props.attribute2 }</h2>
	);
}
```
<br>

The difference is that, ***props*** is a JavaScript Object. 

So, instead of defining many different *parameters* for a Component, all the *params* to be used in the Component are grouped under one Object, ***props***.

![[Pasted image 20231116134258.png]]


Next comes, calling the function.

In JavaScript, arguments are passed to the function when calling it.
```js
func(arg);
```
<br>

> [!info] Recall
> `phrase` is a **parameter** or ***param***.
> ```js
> function greet(phrase) {
> 	console.log(phrase);
> }
> ```
> 
> `"Hello"` is an **argument**.
> ```js
> greet("Hello");
> ```

<br>


In React, these *arguments* or ***attributes*** are mentioned while rendering the component.
```jsx
<Component attribute1="someValue" attribute2="someValue" />
```

Here `someValue` will be the value of `attribute1`. The HTML code would, therefore, look like, 
```html
<h1>someValue</h1>
```
<br>

>[!tip]
>In React, using Functional Components is just like creating JavaScript functions but with different *terminology* or *choice of words*.
>
>| Vanilla JavaScript | React |
>|--|--|
>| Declaring a Function | Creating a Component |
>| Calling the Function | Rendering the Component |
>| Passing Arguments to the Function | Passing Attributes to the Component |