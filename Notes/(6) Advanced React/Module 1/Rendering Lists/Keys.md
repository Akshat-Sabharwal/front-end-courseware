Just like the **keys** of a JavaScript Object, ***keys*** in React are used as *identifiers* or *IDs* for the React components.
<br>


>[!info] The Diffing Algorithm
>
>Let there be an unordered HTML list.
>
>If another item is added in the `<ul>`, React would compare the previous **VDOM** with the updated one. The changes will be then made into the **Real DOM**.
>
>
>
>![[Pasted image 20231121145301.png|500]]
>
>
>This is called the ***Diffing* Algorithm**.

<br>

### The What
**Keys**, in React, are used to create an ***identity*** of a component. Primarily, it is used to make the ***Diffing* Algorithm** a lot more efficient.

### The How
Keys helps React in *remembering* the elements.

Say, in the above example, the item to be added in the list is added at the top and not the bottom.

```jsx
<ul>
	<li>Item 5</li>
	<li>Item 1</li>
	<li>Item 2</li>
	<li>Item 3</li>
	<li>Item 4</li>
</ul>
```

This will confuse the *Diffing* algorithm as it treats the last element as the appended one, always. So, instead of updating just the item appended in the VDOM, it will update the complete the list because the first item is not what it was earlier.

### Application
Keys can be added to a React component using the `key` attribute.
```jsx
const keys = ["five", "one", "two", "three", "four"];;

<ul>
	// Mapping the IDs in the keys list to actual <li> elements with keys 
	{keys.map((key, index) => {
		<li key={ key }>Item {index}</li>
	})}
</ul>
```

<br>

> [!tip]
> It is a good practice to use **keys** that are always unique. Using indexes of list items is not recommended because even on re-ordering the components, the previous order is maintained.
> 



