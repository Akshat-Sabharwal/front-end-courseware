***Pseudo-elements*** are basically ***parts of the HTML elements***. **Pseudo-**, because these are not actual elements but *parts of the elements*.


Some of the most used ones are,
* ##### `::marker`
Creates and stylizes bullet points in a text.

  ```css
p::marker {
	content: '>';
	color: blue;
}
  ```
  <br>
  
* ##### `::first-letter`
Stylizes the first letter of a text

  ```css
  p::first-letter {
	  color: orange;
	  font-size: 4rem;
  }
  ```
<br>

* ##### `::first-line`
Stylizes the first line in a text.

  ```css
  p::first-line {
	  color: aqua;
	  font-style: underline;
  }
  ```
<br>

* ##### `::selection`
Stylizes the text which is selected by the user.

  ```css
  p::selection {
	  background-color: teal;
  }
  ```
<br>

* ##### `::before` and `::after`
Creates and styles a component before the element and after the element.

  ```css
  p::before {
	  content: 'Start';
	  color: red; 
  }
  
  p::after {
	  content: 'End!!';
	  color: green;
  }
  ```
<br>

### Pseudo-Classes
Pseudo-classes are **the different states of HTML elements**. These states can be stylized using selectors.

* When a button is being clicked
* A link that has been visited
* A checkbox which has been checked

##### Syntax
```css
selector:pseudo-element {
	/* CSS rule here */
}
```

| Code | What it means |
|--|--|
| `selector` | The HTML element whose pseudo-element needs to be stylized |
| `pseudo-element` | The pseudo-element that needs to be stylized |


### Some Pseudo-Elements
Pseudo-elements can be categorized for different HTML elements.

* ##### User Actions States
  | Pseudo-class | When does it stylize | Example |
  |--|--|--|
  | `:hover` | Stylizes the state of the element when it is hovered over | `.item::hover { background-color: green; }` | 
  | `:active` | When the button is being clicked | `.item::active { border: 3px solid green; }` |
  | `:focus` | When an element such as `<input>` gets clicked on for user input | `.item { font-size: 3rem; }` |
  
* ##### Form States
  | Pseudo-class | When does it stylize | Example |
  |--|--|--|
  |  |  |  |
* ##### Position-Based States
