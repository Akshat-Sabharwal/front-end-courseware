Imagine that you have a chance to hire a chef to prepare dishes. Instead, of hiring multiple chefs for different dishes,

![[Pasted image 20231123210609.png|320]]


A single chef could be hired who would make all the dishes. 

![[Pasted image 20231123205448.png|350]]


In React, 
* **Chef** → State variable
* **Dishes** → Functions that use state variables

For multiple dishes, multiple state variables must be used which makes the code very vast and messy. The `useReducer` hook is the best fit, here.

### Working
The `useReducer` hook is just like `useState` but more capable. It can implement multiple functions depending upon the need.

Say, for instance, the above scenario is re-created, programmatically. The `useReducer` hook *maps* the elements with functions that are pre-defined. 

![[Pasted image 20231123212254.png|300]]

If `Pizza` was to be selected,
* The `<button>` will ***dispatch*** or *send* the * **type** of dish* selected to a function
* This function will then use an `if..else` statement to look for *what to execute* for this *dish **type** *
* The function will then log `Pizza being prepared...` in the console.


![[Pasted image 20231123220022.png|500]]


### Application
To, finally, create the above scenario in code, 

```jsx
import { useReducer } from "react";

function App() {
	const initialState = { type: null };
	const [state, dispatch] = useReducer(reducer, initialState);
	
	function reducer(action, state) {
		if (action.type === "pizza") {
			console.log("Pizza being prepared...");
		} else if (action.type === "smoothie") {
			console.log("Smoothie blending...");
		} else if (action.type === "taco") {
			console.log("Taco being wrapped...");
		}
	};
	
	return (
		<button 
		  id="pizza" 
		  onClick={ dispatch({ type: "pizza" }) }
		>
		Pizza
		</button>
		
		<button 
		  id="taco" 
		  onClick={ dispatch({ type: "taco" }) }
		>
		Taco
		</button>
		
		<button 
		  id="smoothie" 
		  onClick={ dispatch({ type: "smoothie" }) }
		>
		  Smoothie
		</button>
	);
}
```
<br>

Here, 

| Code | What it means |
|--|--|
| `state` | It is just like state variable in `useState` |
| `dispatch` | It is like the updater function which sends data to `reducer` |
| `reducer` | A function  which *reduces* the action to one of the given cases |
| `initialState` | Just like the argument given to `useState` hook |

