To create a `Header` component which displays the Brand name and its motto,

* **Create the `Header` Component**
```jsx
// Header.jsx

function Header() {
	return(
	);
}
```

* **Add in the HTML Elements**
```jsx
// Header.jsx
function Header() {
	return(
		<div>
			<h1></h1>
			<p></p>
		</div>
	);
}
```

*  **Add the *Props* and its Properties**
```jsx
// Header.jsx
function Header(props) {
	return(
		<div>
			<h1>{ props.brandName }</h1>
			<p>{ props.motto }</p>
		</div>
	);
}
```

* **Export and Import**
```jsx
// Header.jsx
export default function Header(props) {
	return(
		<div>
			<h1>{ props.brandName }</h1>
			<p>{ props.motto }</p>
		</div>
	);
}
```

```jsx
// App.js
import Header from "./components/Header.jsx"

function App() {
}
```

* **Render the Component**
```jsx
// App.js
import Header from "./components/Header.jsx"

function App() {
	<Header />
}
```

* **Add in the Attributes**
```jsx
// App.js
import Header from "./components/Header.jsx"

function App() {
	<Header brandName="Open Tech" motto="Keep Teching"/>
}
```

