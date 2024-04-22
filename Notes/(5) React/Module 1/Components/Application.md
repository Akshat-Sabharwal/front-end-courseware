Say, in order to create a `Heading` component, a series of steps can be followed.
<br>

* #### Create a Component File
This can be done via the terminal.
```shell
touch Heading.js
```
<br>

* #### Code the Component
```jsx
function Heading() {
	return(
		<h1>Hello World</h1>
		<p>This is a React component</p>
	);
}
```
In this case, the code won't work because there are two elements `<h1>` and `<p>` inside one component which is invalid.

Instead of using a `<div>` as a container for `<h1>` and `<p>`, a better option would be a **Fragment**.
```jsx
function Heading() {
	return(
		<>
			<h1>Hello World</h1>
			<p>This is a React component</p>
		</>
	);
}
```

>[!info]
>A **Fragment**, `<></>`, is a special feature only in React that groups multiple elements.

<br>

* #### Export it
The next step is to let the **root component** access the `Heading` component to add it into the webpage.

```jsx
export function Heading() {
	return(
		<>
			<h1>Hello World</h1>
			<p>This is a React component</p>
		</>
	);
}
```

>[!tip]
>The keyword `default` can be used when the component name, `Heading` in this case, and the file name, `Heading.js` here, are the same, which they are in this case.
>```js
>export default function Heading() {
>	// JS code here
>}
>```

<br>

* #### Import it
In order to display the `Heading` component in the webpage, it must be added to the **root component** by importing it in the **root component's file**.

```js
// index.js

import Heading from "./Heading"
```

| Code | What it means |
|--|--|
| `import` | Bring the component in this file |
| `Heading` | Name of the component |
| `"./Heading"` | The path of the file wherein the component is stored, `.` means the current working directory or CWD |

<br>

* #### Using the Component
After importing the component in the `App.jsx` file, it must be ***rendered*** or *displayed on the webpage*.

```jsx
function App() {
	<Header />
}
```

The `Header` component is added in the `App` component as a **self-closing tag**. 