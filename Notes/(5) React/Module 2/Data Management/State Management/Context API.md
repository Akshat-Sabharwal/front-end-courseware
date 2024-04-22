It is quite different from the other two.

### Concept
Say, you have to convey a message to the students in different classrooms.

Going into each room, one-by-one, would be very inefficient.

![[Pasted image 20231118134844.png|450]]


A better way would be to post the message on a notice board outside and let the students read the message, themselves.


![[Pasted image 20231118135432.png|450]]


This is the approach of Context API. Simply put, all the State variables to be used are stored in a separate file. Any component can access the State variables in the file and use, according to need. 


![[Pasted image 20231118135846.png|400]]


### Approach
Using Context API involves multiple steps and files.


* ##### Creating the Context
**Context** is basically the data that can be accessed by all the components which needs to be stored in a separate file.


  ![[Pasted image 20231118155422.png|400]]
<br>

* ##### Providing the Context
The context created is then imported into the Root component file. 

  It is further *wrapped around* the components that need to access the data inside. Much like [[Front-End/(2) JavaScript/Module 3/Paradigms/FP/Scope/Concept|scope]] in JavaScript, the components in the *scope* of the context can use it. 

  This is called ***providing the context***.


  ![[Pasted image 20231118175407.png|500]]
<br>


* ##### Consuming the Context
Components ***consume*** the data in the State variables stored in the context using the `useContext()` hook, just like `useState()`. 

  ![[Pasted image 20231118173620.png|450]]



### Application
This is an implementation of a Context API for the [[Prop-Drilling#Example|example]] of `FuelTank` and `Drives`.

* ##### Creating the Context
```jsx
// Context.jsx
import { createContext } from "react";

// Create a knowledge base, and store the following data
const DataContext = createContext();

export default DataContext
```
<br>

* ##### Providing the Context
```jsx
// App.jsx
import { useState } from "react";
import DataContext from "./Context";

function App() {
	// Creating a "variable" to store the data because data in the context can change
	const [data, setData] = useState({drivesLeft: 10, fuelLeft: 100});

	// Provide the following components the access to this knowledge-base
	<DataContext.Provider value={data}> 
		<Component />
	</Data Context.Provider>
}
```
<br>

> [!info]
> The data to be stored in the Context wasn’t stored while creating it.
>  
> It is passed as an attribute to `<DataContext.Provider>` *via* `value` so that the data can be modified by the components using it.

<br>


* ##### Consuming the Context
```jsx
// Drives.jsx
import DataContext from "./Context";
import { useContext } from "react";

const Drives = () => {
	// Use the context and extract the data from it.
	const { drivesLeft } = useContext(DataContext);
	
	return (
		<h1>Drives Left: { drivesLeft }</h1>
	);
}
```