A button, when clicked, should perform an action. That's what the function of a button is.

An action done by the user is considered an **Event**. What takes care of *what, then, should be done* is called a **Handler**.

### Events in React
React allows for numerous **events** to be *handled*. For instance,

| Event | What  it means |
|--|--|
| `onClick` | When an element is clicked, an action is performed |
| `onMouseOver` | On hovering over an element, an action is performed  |
| `onCopy` | When something is copied, an action is performed |

There are many such events in React and HTML.

### Syntax
Event Handling is supported by, both, [[Event Handling|HTML]] and React. In React, there are 3 ways to handle an event.
<br>

* **Using a plain function**
The function is first declared and then assigned to the `onClick` attribute inside *curly-braces* `{}`.

  ```jsx
function Button() {
	const displayMessage = () => console.log("Button was pressed!");
	
	return (
		<button onClick={displayMessage}></button>
	);
}
  ```

* **Declaring an arrow function, therein**
The arrow function is declared as the value of the `onClick` attribute.
  ```jsx
  function Button() {
	return (
		<button onClick={() => console.log("Button was pressed!")}></button>
	);
}
  ```
  
* **Declaring a plain function, therein**
The plain function is declared as the value of the `onClick` attribute.
  ```jsx
  function Button() {
	return (
		<button onClick={function() { console.log("Button was pressed!")}}></button>
	);
}
  ```

### Example
When hovered over a `<div>` container, log the message `Hovering over the div` in the console.

```jsx
function EventHandler() {
	return (
		<div onMouseOver={() => console.log("Hovering over the div")}></div>
	);
}
```