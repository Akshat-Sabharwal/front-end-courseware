There are numerous APIs that React provides to create a web app. Two such are, `cloneElement` and `Children`.

### `cloneElement`
As the name suggest, it is used to clone React **elements**. It takes in a React component, creates a clone of the component and adds in the desired *props* to it.

##### Example
Say, a `Button` component has 2 *props*, `type` and `children`. `type` is initially set to `null`.
```jsx
function Button({type, children}) {
	return (
		<button key={type} >{children}</button>
	);
}

function App() {
	const loginButton = React.cloneElement(<Button />, {type: "login"});
	const signupButton = React.cloneElement(<Button />, {type: "signup"});
	
	return (
		{loginButton}
		{signupButton}
	);
}
```

Here, the 2 clone of the `Button` component are created as the `type` for each of them was to be different.
<br>

### `Children`
It is used to access the `childrens` *prop* of a React **element** and dynamically modify it. 

Various operations can be done using the `Children` API. One such is `map()` which is just like *mapping* JavaScript lists.

##### Example
This changes the font color of each child of the component to `red`.
```jsx
function Items({children}) {
	return (
		{React.Children.map(children, (child) => {
			React.cloneElement(child, 
				{
					style: {
						...child.props.style,
						color: "red",
					}
				}
			)
		})}
	);
}

function App() {
	return (
		<Items>
			<p>This</p>
			<p>is</p>
			<p>React</p>
			<p>API</p>
		</Items>
	); 
}
```