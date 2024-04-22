JavaScript is used to add interactivity to websites and this is where it begins. Handling events basically means to *look out for any interaction made by the user*. 

### Click or Tap
Say, you are building a webpage which accepts user input and prints it in the console on the click of a button. How will the button know what to do?

One way of assigning a function to a button is using the `addEventListener()` method.
It takes in two arguments. 
*  Type of event, click in this case
*  The function to assign the component.

#### Example
A button can be assigned a function of printing `Hello World!` in the console.
```js
function print() {
	console.log("Hello World!");
}

const btn = document.querySelector('button');
btn.addEventListener('click', print);
```

The second method is by adding the `onClick` attribute to the element in the HTML document itself.

```js
// index.js
function print() {
	console.log("Hello World!");
}
```

```html
%% index.html %%
<button onClick="print()">Print<button>
```
