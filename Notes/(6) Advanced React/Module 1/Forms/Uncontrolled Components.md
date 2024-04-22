They are the counterpart of Controlled Components.

[[Controlled Components#^74ced6|Herein]], instead of the teacher keeping the record of the students, the students, themselves, check if they are still a part of the group or have been lost.


![[Pasted image 20231122183853.png|400]]


Here, 
* **Students** → Uncontrolled Components
* **Presence Record** → The *data* or *state* of the components

The *students* take care of the *presence record*, themselves. In other words, the data of the Uncontrolled components is stored **in** the components. This makes the system **decentralized**.

### Working
Uncontrolled components are way more easier to deal with. Say a [[Controlled Components#Working|similar]] Authentication form has been created using Uncontrolled components.

When the *Username* is entered in the field,
   
* The input in the *Username* field will be ***pulled*** or *retrieved*.
* This value can then be used wherever wanted.

It’s that simple.

### Application
To do so, 

* ##### Create the Components
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
<br>


* ##### *Pull* the Input
The input is retrieved using the `useRef` hook. It is initialized with a value which can be accessed using the `current` property. This value can be *mutated* or *changed*, as well.

  ```jsx
  import { useRef } from "react";
  
  export function Form() {
	const usernameRef = useRef(null);
	const passwordRef = useRef(null);
	
	return (
		<form>
			<label forHtml="username">Username: </label>
			<input
				type="text"
				id="username"
				ref={usernameRef}
			/>
			  
			<label forHtml="password">Password: </label>
			<input
				type="password"
				id="password"
				ref={passwordRef}
			/>
		</form>
	);
  }
  ```