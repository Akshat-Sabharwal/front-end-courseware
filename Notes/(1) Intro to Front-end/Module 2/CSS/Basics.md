CSS stands for **Cascading Style Sheet** and serves the function of styling an HTML document or simply, a webpage.

## Syntax
Each element in an HTML document can be styled separately and collectively. Below is called a **CSS Rule**.

```CSS
p {
	color: green;
	font-size: 2em;
}
```

| Component | Function |
|--|--|
| `p` | Stylize all elements with this tag called the **Selector** |
| `{}` | Contain the style declaration block |
| `color` | The property that needs to be modified |
| `green` | The value of the property to be modified |

#### Selector
In a CSS rule, the tag name before the opening curly bracket is called a **selector**. It *selects* the elements of a tag to be modified.

##### CSS Precedence and Specificity
A property of CSS which allows the user to modify specific elements by using different selectors.

| Property | ID Selector | Class Selector | Descendant Selector |
|--|--|--|--|
| Usage | Modifies all elements with same `id` attribute | Modifies all elements with the same `class` attribute | Modifies all elements with a specified tag within another tag |
| Syntax | Use a `#` before the selector | Use a `.` before the selector | Use `#id_of_parent element > tag_to_modify` |
| Example | Sets the color of all elements with `id` as `para_id` to green <br> ![[Pasted image 20230926144947.png]] | Set the color of all elements with `para_class` as the attribute of `class` to green <br> ![[Pasted image 20230926145000.png]] | Sets the color of all `<p>` elements within the `para_class` element to green <br> ![[Pasted image 20230926145033.png]] |

  

