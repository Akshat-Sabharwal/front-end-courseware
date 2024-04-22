Imagine being a teacher who has to look after the students on a picnic. A good way of ensuring that every student is present at all times would be to maintain a record of the students by calling  for each student at regular intervals.  ^74ced6

![[Pasted image 20231122135146.png|450]] ^a9e4a9


Here, 
* **Teacher** → React code
* **Students** → Controlled Components
* **Presence Record** → State of the Controlled Components

The React code ***controls*** or *keeps track of* the state of the components. The components whose state is being **controlled** by React are **Controlled Components**. Thus, the data stored is **centralized**.

Also, whenever any change is made to the components’ state, React *reflects* or *shows* it in the compiled React app. 


![[Pasted image 20231122140111.png]]


Just like, if any student got lost, it would be immediately be recorded and his search would begin.


### Working
Controlled Components are, generally, used with forms. 

Therefore, say for instance, an Authentication form has been created using Controlled Components. When the *Username* is entered in the field, 

* The *Username* entered will be updated to the State variable linked to the component.


  ![[Pasted image 20231122143316.png|550]]
  <br><br>
  
* The `value` attribute of the *Username* `<input>` element will be updated to the value of the State variable.


  ![[Pasted image 20231122144114.png|550]]

<br>

>[!info]
>`value` is an attribute of the `<input>` element. Its value is what is displayed inside the field. 
>
>If the `value` is set to `Default`, despite of whatever may be typed in the field, `Default` will be shown.
>
Also, the `value` will not store what was typed in this case.

<br>

### Application
To achieve the proper working of a simple Authentication form created using controlled components,  

* ##### Create the Input Elements
Two elements for *password* and *username* are to be created.
  ```jsx
  export function Form() {
	return (
		<form>
			<label forHtml="username">Username: </label>
			<input
				type="text"
				id="username"
			/>
			  
			<label forHtml="password">Password: </label>
			<input
				type="password"
				id="password"
			/>
		</form>
	);
  }
  ```
  <br><br>
  
* ##### Create the State Variables 
A State variable for each of the `<input>` elements are to be created to store the input.
  ```jsx
  import { useState } from "react";
  
  export function Form() {
	const [username, setUsername] = useState("");
	const [password, setPassword] = useState("");
	  
	return (
		<form>
			<label forHtml="username">Username: </label>
			<input
				type="text"
				id="username"
			/>
			  
			<label forHtml="password">Password: </label>
			<input
				type="password"
				id="password"
			/>
		</form>
	);
  }
  ```
  <br><br>
  
* ##### Sync the System
***Syncing the system***, here, means *to create a system which would automatically update the values to the current input*.

  This is done by assigning the `value` and `onChange()` attributes to the `<input>` elements. 
  
  `onChange` is another Event Handler like `onClick` which is triggered whenever any character is added or deleted from the input field. 
  
  ```jsx
  import { useState } from "react";
  
  export function Form() {
	const [username, setUsername] = useState("");
	const [password, setPassword] = useState("");
	  
	return (
		<form>
			<label forHtml="username">Username: </label>
			<input
				type="text"
				id="username"
				  
  // The username State variable's value will be displayed in the input field
				value={username}
				  
  // It says, update the state variable's value to the current input
				onChange={(event) => setUsername(event.target.value)}
			/>
			  
			<label forHtml="password">Password: </label>
			<input
				type="password"
				id="password"
				value={password}
				onChange={(event) => setPassword(event.target.value)}
			/>
		</form>
	);
  }
  ```

> [!info]
> `event` is a JavaScript Object which carries all the information about an [[Events and Handlers|event]] that has occurred.
> 
> For instance, 
> 
> ![[Pasted image 20231122162111.png|300]]
> 
> The above event was a `click` on the `<button id="someButton">` at the coordinates `(100, 200)px`.





