Just the same as Prop-drilling. 

The only difference is that the data to be passed *via* *props* is stored in State variables whereas in Prop-drilling, the data is stored in JavaScript containers and objects. 

### Example
Executing the same example as Prop-drilling, just with States. 

* **Creating the Components**
  ```jsx
  // FuelTank.jsx
  export const FuelTank = (props) => {
	  return (
		  <h1>Fuel left: { props.fuelLeft }</h1>
	  );
  }

  // Drives.js
  export const Drives = (props) => {
	  return (
		  <h1>Drives left: {props.drivesLeft}</h1>
	  );
  }

  // App.js
  import { Drives } from "./components/Drives"
  import { FuelTank } from "./components/FuelTank"
  
  export const App = () => {
	  return (
		  <Drives />
		  <FuelTank />
	  );
	}
  ```



* **Storing the Data**
  ```jsx
  // App.js
  import { Drives } from "./components/Drives"
  import { FuelTank } from "./components/FuelTank"
  import { useState } from "react"
  
  export const App = () => {
	  const [fuelLeft, setFuelLeft] = useState(100);
	  const [drivesLeft, setDrivesLeft] = useState(10);
	  
	  const data = {
		  fuelLeft, 
		  setFuelLeft,
		  drivesLeft,
		  setDrivesLLeft,
	  }; 
	  
	  return (
		  <Drives />
		  <FuelTank />
	  );
	}
  ```

* **Drilling *via* *Props***
  ```jsx
  // App.js
  import { Drives } from "./components/Drives"
  import { FuelTank } from "./components/FuelTank"
  import { useState } from "react"
  
  export const App = () => {
	  const [fuelLeft, setFuelLeft] = useState(100);
	  const [drivesLeft, setDrivesLeft] = useState(10);

	  const data = {
		  fuelLeft, 
		  setFuelLeft,
		  drivesLeft,
		  setDrivesLLeft,
	  }; 
	  
	  return (
		  <Drives {...data} />
		  <FuelTank {drivesLeft, setDrivesLeft} />
	  );
	}
  ```
