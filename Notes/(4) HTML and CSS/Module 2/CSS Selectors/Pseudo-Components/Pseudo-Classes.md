There are mainly four categories of pseudo-classes.

### User Action States
It is just a fancy phrase for *any action done by the user*. Thus, whenever a user performs a specific action, it changes the state of an HTML element. This state can be stylized.

* #### `:hover` 
Whenever the user **hovers** or *brings its cursor onto an element*, the `hover` state gets triggered and displayed.

  ###### Example
  This will change the `background-color` of the button to `darkblue` when it is hovered over.
  ```css
  .btn:hover {
	  background-color: darkblue;
  }
  ```
  <br>
  
* ##### `:active`
When a button, or element alike, is **being** clicked, its state at that point is ***active***.

  ###### Example
  This will create `aqua` colored borders of the button during the click.
  ```css
  .btn:active {
	  border: 3px solid aqua;
  }
  ```
  <br>
  
* ##### `:focus`
When an input field or element alike is clicked to enter the data, it is said to be in the **focused** state.

  ###### Example
  This will increase the `font-size` to `3rem` when the input is being entered.
  ```css
  .btn:focus {
	  font-size: 3rem;
  }
  ```
<br>

### Form States
There are pseudo-classes specifically for the input-fields in forms.

* ##### `:disabled`, `:enabled`
It is, primarily, used to stylize buttons which are **disabled** which are *unclickable* or **enabled** which are *clickable*.

  ###### Example
  This will make the disabled button have a lower opacity which is *visibility of an element*.
  ```css
  .btn:disabled {
	  opacity: 0.6;
  }
  
  .btn:enabled {
	  opacity: 1;
  }
  ```
  <br>
  
* ##### `:checked`, `:indeterminate`
Used with checkboxes.

  ###### Example
  This will change the text to a strike-through one if the checkbox is checked else it will remain the same.
  ```css
  .checkbox:checked {
	  font-style: line-through;
  }
  ```
  <br>
   
* ##### `:valid`, `:invalid`
Used with input fields like `number` and `email` which tolerate only certain formats which are considered **valid**. Any other format is considered **invalid**.

  ###### Example
  This will highlight the input field with green borders if the input is valid else red borders.
  ```css
  .checkbox:valid {
	  border: 3px dash green;
  }
  
  .checkbox:invalid {
	  border: 3px dash red;
  }
  ```
  <br>
### Position-Based 
These pseudo-classes are like, or in fact **are** [[Selectors|child selectors]]. `:nth-type()` is one of such classes. 

* ##### `:nth-of-type()`
The same functionality as `nth-type()`. Selects the component of mentioned type at the given position.

  ###### Example
  Selects all the `<h2>` elements at even position numbers.
  ```css
  h2:nth-of-type(even) {
	  /* CSS rule here */
  }
  ```
  <br>
  
* ##### `:nth-last-of-type()`
Same as `nth-of-type()`. The difference is that it starts from the end. 

  ###### Example
  This selects the second-last `<p>` element.
  ```css
	  p:nth-last-of-type(2) {
		  /* CSS rule here */
	  }
  ```
  <br>
  
* ##### `:first-of-type()`
Selects the first element of the given type.
<br>

* ##### `:last-of-type()`
Selects the last element of the given type.