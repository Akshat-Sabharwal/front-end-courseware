Herein, the data to be accessed by the Sibling components is contained in the Parent component.
The data is then passed to the Children components *via* *props*.


![[Pasted image 20231118132602.png|350]]


`Drives` needs `fuelLeft` for the calculation and thus, it accepts both of them. `FuelTank` doesn’t rely on `drivesLeft`. Thus, it only imports what’s required.


### Example
Executing the above example, programmatically, would be quite tedious. A relatively simpler one would be,

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
  
  export const App = () => {
	  const data = {
		  fuelLeft: 100,
		  drivesLeft: 10,
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
  
  export const App = () => {
	  const data = {
		  fuelLeft: 100,
		  drivesLeft: 10,
	  };
	  
	  return (
		  <Drives {...data} />
		  <FuelTank fuelLeft={data.fuelLeft} />
	  );
	}
  ```

<br>

>[!tip]
>When all the properties of an object are to be used, the [[Some operators#Rest Operator|Rest operator]] can be used.
>```jsx
>const data = {
>	someProp1: “someValue1”,
>	someProp2: “someValue2”,
>	someProp3: “someValue3”,
>};
>
><Component  {…data} />
>```


