Simply put, they are JavaScript functions to initialize, access and modify a React component’s state.


![[Pasted image 20231118154831.png|600]]


### Hooks in React
There are many pre-defined **hooks** in React for different purposes. 

* `useState`
* `useEffect`
* `useMemo`

…and much more. The most used, however, is `useState`.

### `useState`
It is a hook to ***create and update state variables***.

##### Syntax
Here, [[Some operators#^4911b4|array deconstruction]] is used because `useState()` returns an array with a variable and an updater function, essentially a JavaScript function. 
```jsx
const [stateVariableName, setStateVariableName] = useState(initialValue);
```

| Code | What it means | Example |
|--|--|--|
| `stateVariableName` | Name of the state variable to be *created* or *initialized* | `isTrue` |
| `setStateVariableName` | Name of the function to update the state variable | `setIsTrue` |
| `initialValue` | The initial value of the state variable, `stateVariableName` in this case | `true` |


### Example
Recreating [[State#Example|this example]] using code,
```jsx
export const Car = () => {
	const [hasStarted, setStart] = useState(false);
	const [isFuelOver, setFuelOver] = useState(true);
	const [distance, setDistance] = useState(102);

	return (
		<>
			// When clicked, sets the value of hasStarted to false
			<button 
			onClick={() => {setStart(true); console.log(hasStarted)}}>
			Start
			</button>

			// When clicked, sets the value of hasStarted to true
			<button 
			onClick={() => {setStart(false); console.log(hasStarted)}}>
			Stop the Car
			</button>
		</>
	);
} 
```

Here, the approach is to 
* First, create a component
* Initialize its State variables

For adding functionality to component using the state variables,
* Use the Event Handler `onClick` on the `<button>` element
* Declare a function which updates the State variable using the Updater function

<br>

>[!note]
>The Updater function cannot be called directly. 
>```jsx
>const Component = () => {
>	const [data, setData] = useState(“some data”);
>	
>	// Like so
>	setData(“some other data”);
>}
>```
>
>It must be an action of an event.
>```jsx
>const Component = () => {
>	const [data, setData] = useState(“some data”);
>	
>	// Like so
>	return (
>		<div onMouseOver={() => {setData(“some other data”);}}></div>
>	);
>	
>}
>```