HTML also supports and avails built-in structures for data management.

## Lists
An element in HTML for displaying point-based data. 
HTML supports two broad types of lists.

- ##### Ordered List
List with bullet points as numbers or index-based bullets.
<ol>
	<li>Apple</li>
	<li>Pineapple</li>
	<li>Custard Apple</li>
</ol>

```html
<ol></ol> acts as a container of the ordered list
```

- ##### Unordered List
List with basic bullet points.
<ul>
	<li>Apple</li>
	<li>Pineapple</li>
	<li>Custard Apple</li>
</ul>
 ```html
<ul></ul> acts as the container of an unordered list
```


## Table
Unlike regular tables, tables in HTML aren’t represented in a purely tabular format but somewhat resembles it.

<table>
	<tr>
		<td>A1</td>
		<td>A2</td>
	</tr>
	<tr>
		<td>B1</td>
		<td>B2</td>
	</tr>
</table>

```html
<table>
	<tr>
		<td>A1</td>
		<td>A2</td>
	</tr>
	<tr>
		<td>B1</td>
		<td>B2</td>
	</tr>
</table>
```

```html
<table> contains the rows and columns
<th> is for the table header
<tr> is for the table row
<td> is for the table data
```

The approach to filling out the table is to work your way row-wise.

* ###### Row A
    - `<tr>`
    - Cell A1 or `<td>A1</td>` is added
    - Cell A2 or `<td>A2</td>` is added
    - `</tr>`

* ###### Row B
    - `<tr>`
    - Cell B1 or `<td>B1</td>` is added
    - Cell B2 or `<td>B2</td>` is added
    -  `</tr>`


## Forms
Pre-built and structured modes of obtaining user input via HTML.  

<form action=/authorization method=POST>
	<label for=username>Username:</label>
	<input type=text id=username>
	<br>
	<label for=password>Password:  </label>
	<input type=password>
</form>


```html
<form action=/authorization method=POST>
	<label for=username>Username:</label>
	<input type=text id=username>
	<br>
	<label for=password>Password:  </label>
	<input type=password>
</form>
```



| Component | Function |
|--|--|
| `<form>` | Encapsulates the contents of the form |
| `<input>` | Prompts for input from user |
| `<label>` | A description of what to do |

#### Input Types

| Type | Function |
|--|--|
| `text` | Input text from user <br> <input type=text>|
| `password` | Inputs hidden text from user <br> <input type=password>|
| `checkbox` | Input the choices of user from given options <br> <input type=checkbox value=Option1> <label for=Option1>Option 1</label> <br> <input type=checkbox value=Option2><label for=Option2>Option 2</label>|
| `radio` | Input a single choice from user <br> <input type=radio name=Option><label for=option1>Option 1</label> <br> <input type=radio name=Option><label for=Option2>Option 2</label>|
| `file` | Input a file from the user <br> <input type=file>  |
| `email` | Input email of correct format from user <br> <input type=email pattern=“.+@gmail\.com”> |

#### Some other Input Elements
These elements are not attributes of the `<input>` tag but rather are tags themselves used for taking user input

| Element | Function |
|--|--|
| `textarea` | Input lengthy text from user <br> <textarea></textarea>|
| `select` | Input the choice of user from a drop-down menu <br> <select name=food><option value=burger>Burger</option><br><option value=Pizza>Pizza</option></select> |
#### Attributes

* #### `<form>`
	* `action` → The address to forward the input
	* `method` → The HTTP method to use

* #### `<input>`
	* `name` → Name of the input element
	* `id` → Identity to denote the element
	*  `type` → The mode of input

* #### `<label>`
	* `for` → The element for which the label is
	* `id` → Identity to denote the label
