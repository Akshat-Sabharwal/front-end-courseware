Objects used to select items are called **selectors**. 

In CSS, it is the same way. In order to tell the computer, which CSS rule should be applied to which HTML element, CSS selectors are used.

There are numerous of them.
<br>

* ### Element Selector
Selects all the elements of a certain type. 

  ##### Example
Selects all the `<p>` elements in an HTML file.
  ```css
p {
	/*CSS rule here*/
}
  ```
<br>

* ### ID Selector
Selects the element with the specified ID. It selects only 1 component because ID is unique to every element.

  ##### Example
  Selects the element with `id="paragraph"`.
  ```css
#paragraph {
	/*CSS rule here*/
}
  ```
<br>

* ### Class Selector
Selects all the elements with the specified class name because multiple elements can have the same class name.

  ##### Example
  Selects all the elements with `class="paragraph"`.
  ```css
.paragraph {
	/*CSS rule here*/
}
  ```
<br>

* ### Child Selector
Selects the child component at the specified position.

  ##### Example
  Selects the second `<p>` element and applies the rule to it.
  ```css
p:nth-child(2) {
	/*CSS rule here*/
}
  ```
<br>

* ### Attribute Selector
Selects the element(s) with the specified attribute.

  ##### Example
  Selects the `<a>` element with `href` attribute having the value `https://www.example.com`

  ```css
a[href="https://www.example.com"] {
	/*CSS rule here*/
}
  ```
<br>

* ### Star Selector
Selects all the elements in an HTML file.

  ##### Example
  Applies the font-color `blue` to all the elements within the HTML file.
  
  ```css
  * {
	color: blue;
  }
  ```