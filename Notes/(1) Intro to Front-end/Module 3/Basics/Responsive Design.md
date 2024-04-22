The same websites when viewed on a mobile phone and a laptop differ in the orientation of components and the layout of the webpage. The following are responsible for the same.

## Fluid Images
Images via CSS can be assigned maximum dimensions so they can adjust their size in accordance with the device and its display. 

Say an image of a flower is to be displayed on a webpage. We want the original size of the image if enough space is available else it must adapt itself to the device it's viewed on.

```CSS
img {
	max_width: 100%;
}
```

This makes the image adjustable or **fluid**.

## Flexible Grids
Just like fluid images, content grids, too, can be **fluid** or **flexible**. They instead of the conventional `width` and `height` CSS declarations, are associated with a percentage of the space on the webpage.

![[Pasted image 20230912220813.png]]

| Parts | Structure | Reference |
|--|--|--|
| Gutter | The space between consecutive content grids | The blue line |
| Margins | The space between the browser window and the content grid | The black lines |
| Columns | The grids of content | The grey area |


## Media Queries
These are CSS rules to specify the orientation and layout of a webpage beforehand using CSS. Each condition which triggers the use of the specified rule is called a **Breakpoint**. 
#### Desktop

```CSS
@media only screen and (min-width: 700px) {
	.col-1 {
		width: 33.33%;
	}
	.col-2 {
		width: 33.33%;
	}
	.col-2 {
		width: 33.33%;
	}
}
```

The **media query** above specifies that the width of each column must be ⅓ (*one-third*) of the total space available on the webpage.

Also, `@media only screen and (min-width: 700px)` this basically means that any screen with a minimum width of 700px must have this layout.  This is the **breakpoint** for the layout.

| Keyword | Meaning |
|--|--|
| `@media` | To indicate a media query block |
| `only screen` | To indicate the target. We want the orientation to be just in case of *screens* and not *print* or *speech* |
| `(min-width: 700px)` | The condition which acts as a trigger point for the code |

#### Mobile

```CSS
@media only screen and (max-width: 700px) {
	[class *='col-'] {
		width: 100%;
	}
}
```

This code `@media only screen and (max-width: 700px)` is the **breakpoint**.

`[class *= "col-"]` declares the same CSS rule for every class-name that begins with *col-* . It can also be rephrased as

```CSS
@media only screen and (max-width: 700px) {
	.col-1 {
		width: 100%;
	}
	.col-2 {
		width: 100%;
	}
	.col-3 {
		width: 100%;
	}
}

```