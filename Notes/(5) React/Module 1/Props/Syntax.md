A ***prop*** is passed as a *param* to the React component. Moreover, its properties can be accessed by the dot-notation inside a [[JSX#Embedded Expressions|JSX embedded expression]]. 

```jsx
function Heading(items) {
	return(
		<h1>{ items.head }</h1>
		<h2>{ items.subHead }</h2>
	);
}
```

>[!tip]
>***Props*** can have any name, just like any other JavaScript Object. It is just a convention to use `props`.

<br>
