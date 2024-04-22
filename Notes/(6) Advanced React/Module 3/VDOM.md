At the time of compilation and rendering, the components created using JSX are converted into plain JavaScript objects called **JSX Elements**.

For instance, the following code,
```jsx
function App() {
	return (
		<Header />
		<Main />
		<Footer />
	);
}
```


would look something like this,
```js
{
	type: "App",
	props: {
		children: [
			{
				type: "Header"
			},
			{
				type: "Main"
			},
			{
				type: "Footer"
			]
		}
	}
}
```

Each component is represented by a JS object with two properties, `type` and `props`. 

| Properties | What it signifies |
|--|--|
| `type` | It’s value is the name of the component |
| `props` | It has more nested properties such as `className` and `children` |

These components are further broken down into the HTML elements they are made of.
```jsx
function Header() {
	return <h1>This is some heading</h1>
}
```

```jsx
{
	type: "h1",
	props: {
		children: [
			{
				"This is some heading"
			},
		]
	}
}
```

This *simplification* or *conversion* of JSX components to **elements** creates the **Virtual DOM**, or **VDOM** for short, which React uses to create the UI.

### Example
A simple React `Form` component would have the following **Elements’ tree**,
```jsx
function Form() {
	return (
		<form>
			<input type="text" placeHolder="Username"/>
			<input type="password" placeHolder="Password"/>
			<input type="submit" id="submit"/>
		</form>
	);
}
```
<br>

```jsx
{
	type: "form",
	props: {
		children: [
			{
				type: "input"
				props: {
					type: "text",
					placeHolder: "Username"
				}
			},
			{
				type: "input"
				props: {
					type: "password",
					placeHolder: "Password"
				}
			},
			{
				type: "input"
				props: {
					type: "submit",
					id: "submit"
				}
			}
		]
	}
}
```