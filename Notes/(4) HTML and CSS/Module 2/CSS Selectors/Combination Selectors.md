As the name suggests, selectors that combine elements are called **combination selectors**.
<br>

* ### Child Selector
Selects the immediate child component of the specified type.
<br>

  ##### Example
  This will select just the text `Hey!` because it is the ***immediate child*** of the `<div>` element.
  ```css
  /* styles.css */
  div h1 {
	  /* CSS rule here */
  }
  ```
  
  ```html
<!-- index.html -->
<div>
	<h1>Hey!</h1>
	<span>
		<h1>How are you doing?</h1>
	</span>
</div>
  ```
<br>

* ### Descendant Selector
It selects the direct child of the element with the specified class or element type.
<br>

  ###### Example
  This selects only `<h1>Hey!</h1>` and not `<h1>How are you doing?</h1>` because the first one is its direct child.
  
  ```css
  /* styles.css */
  div h1 {
	  /* CSS rule here */
  }
  ```
  
  ```html
<!-- index.html -->
<div>
	<h1>Hey!</h1>
	<span>
		<h1>How are you doing?</h1>
	</span>
</div>
  ```
<br>

* ### General Sibling Selector
Selects all the ***siblings*** of the specified element type.
<br>
  ##### Example
  This selects all the `<p>` elements besides `<h1>` as they are ***siblings*** or **children to the same parent element**.
  
  ```css
  /* styles.css */
  h1 ~ p {
	  /* CSS rule here */
  }
  ```
  
  ```html
<!-- index.html -->
<div>
	<h1>Hey!</h1>
	<span>
		<h1>How are you doing?</h1>
		<p>Hoping you are good,</p>
		<p>Let's go  on a trip!</p>
	</span>
</div>
```
<br>

* ### Adjacent Sibling Selector
Selects the immediate next sibling and not all of the siblings.

  ##### Example
  This selects `Hoping you are good,` besides `<h1>` and not all the siblings.
  
  ```css
  /* styles.css */
  h1 + p {
	  /* CSS rule here */
  }
  ```
  
  ```html
<!-- index.html -->
<div>
	<h1>Hey!</h1>
	<span>
		<h1>How are you doing?</h1>
		<p>Hoping you are good,</p>
		<p>Let's go  on a trip!</p>
	</span>
</div>
