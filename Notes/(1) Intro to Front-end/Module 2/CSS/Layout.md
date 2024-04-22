Elements in an HTML document need to be *understood* by the browser to stylize and display them further with CSS. For instance,

```html
<html>
	<body>
		<h1>Hello World!</h1>
	</body>
</html>
```

```CSS
h1 {
	color: rgba(0, 0, 0, 1);
}
```

How does the browser know as to where shall each letter of `<h1>` be located?


## Box Model
Browsers use what’s called a **box model** to solve the above problem. Each HTML element is assigned a bounding box around it.

![[Pasted image 20230909220226.png]]

| Boundary | What it means |
|--|--|
| Content | This is the actual width and height of the content |
| Padding | The space between the content size and its bounding box |
| Border | The width of the border of the bounding box |
| Margin | The space between the complete element and another one alike |


## Document Flow
The bounding boxes to the elements have been allocated but where shall they be positioned on a webpage? 
**Document Flow** specifies the orientation of elements on a webpage.

#### Inline Format
Elements can be specified to have an arrangement such that every next element appears in the same line as the previous or in other words **occupy the space of the content size only**.

![[Pasted image 20230909222305.png]]

This can be done by-
* -choosing elements that are pre-defined as inline elements such  as `<span>` and `<form>`.
* -declaring a CSS rule that specifies the layout

```CSS
h1 {
	display: inline;
}
```

#### Block Format
Elements which always occupy a new line or in other words **have the height of an element and the width of the parent element**.

![[Pasted image 20230909222437.png]]

This can be done by-
* -choosing elements that are pre-defined as block elements such  as `<div>` and `<input>`.
* -declaring a CSS rule that specifies the layout

```CSS
h1 {
	display: block;
}
```


## Alignment
The above models are for positioning the elements but aligning a piece of text is different than setting it to a block-level element.

#### Text
Text can be aligned in CSS by modifying the `text-align` property in broadly four ways.

| Alignment | Visual |
|--|--|
| `left` | <p style="text-align: left">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam</p> |
| `right` | <p style="text-align: right">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam</p> |
| `center` | <p style="text-align: center">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam</p> |
| `justify` | <p style="text-align: justify">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam</p> |

Also, to wrap text around an element the  `float` property is edited via CSS.

<div class="parent">
	<div style="height: 100px; width: 150px; background: rgb(128, 128, 128); float: right;">
	</div>
	<div>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam
	</div>
</div>



#### Element
Aligning elements just requires the following line of code

```CSS
child_span {
	transform: translate(-x%, -y%);
}
```
