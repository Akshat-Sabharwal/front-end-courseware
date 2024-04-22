In order to cook a dish, several tasks need to be done before and after the actual cooking, such as *grabbing ingredients* and *cleaning the kitchen*. 


![[Pasted image 20231123151909.png]]


Although, these tasks are not directly involved in the cooking process, they still are necessary. Such tasks are called ***side-effects***.

In React, ***side-effects*** are processes like *fetching data from some source* and *logging data in the console*.

Also, *grabbing the ingredients for a specific dish* or tasks alike are done only when that dish is to be prepared and not every time a dish is prepared. 


For instance, if a *pie* was baked initially followed by a *taco*, the ingredients of *pie* shouldn’t be bought over again. 

![[Pasted image 20231123152135.png]]

This is the problem with **side-effects**. They keep on repeating after every render in React.

### Working
The `useEffect` hook allows to *separate* the side-effects and control *how frequently should they be executed*. 

`useEffect` takes in two values, *the side-effect* and a ***dependency array***. The **dependency array** is a JavaScript list which contains some states or *props*.

When used, it tells the compiler, *execute the side-effect only if the values of states or props given in the dependency array change*. Re-rendering only the components which are changed makes the webpage more efficient.


### Application
To create a simple webpage which has 2 `<button>` elements, one which executes the side-effect and the other which conditionally renders a `<p>` element.

```jsx
import { useEffect, useState } from "react";

function App() {
  // A state for name
  const [name, setName] = useState("John")

  // A state for a random task that shouldn't invoke the side-effect
  const [toggle, setToggle] = useState(true);

  // It says, "execute this function if there is a change in the value of name state"
  useEffect(() => console.log("Executing side-effect..."), [name]);

  return (
    <>
      <h1>{name}</h1>

	  <!-- If toggle === true, <p> will be rendered, else not -->
      {toggle && <p>This shouldn't execute the side-effect</p>}

	  <!-- Toggling the name to John or Mary-->
      <button onClick={() => setName(name === "Mary" ? "John" : "Mary")}>
        Execute Side-effect
      </button>

	  <!-- Toggling the visibility of the <p> element -->
      <button onClick={() => setToggle(!toggle)}>Doesn't Execute</button>
    </>
  );
}
```
<br>

If  `Execute Side-effect` button is clicked,
* Value of `name` changes to `Mary`
* `useEffect` gets invoked that value of `name` is changed
* Side-effect is executed

If the `Doesn't execute` button is clicked,
* Value of `toggle` changes to `false`
* `useEffect` doesn’t get invoked because the value of `name` state is still the same
* `<p>` gets hidden

