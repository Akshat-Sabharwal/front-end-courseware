This method, too, involves the usage of columns and rows.

### Creating the Areas
To create the areas, first the columns and rows must be defined. 

For instance, for such a layout, the container must be divided into equal rows and columns, first.

![[Pasted image 20231104192437.png]]

Next comes defining which space would an area occupy using a special format.
##### Properties
This is done using the `grid-template-areas` property.
```css
grid-template-areas: "purple purple yellow green"
					 "blue red red green";
```

The value basically says, 
###### In the first row,
* The first two grid cells are to be grouped together and named **purple**.
* The third grid cell is to be named **yellow**.
* The fourth named **green**.

###### In the second row,
* The first grid cell must be named **blue**.
* The next two named **red**.
* The last one to be named **green**.

![[Pasted image 20231104193544.png|350]]

Then, the grid cells with sharing the same name are grouped together.  This forms the desired layout.

![[Pasted image 20231104194336.png|350]]

### Assigning the Areas
Now, the boxes are to be placed in their respective areas.

##### Properties
This is done using the `grid-area` property **which is used on the child component**.
```css
.child {
	background-color: purple;
	grid-area: purple;
}
```

> [!note]
> The name of the area could have been anything. For the sake of simplicity, it has been named `purple`.


The `grid-area` assigns the box to the area named `purple`. This, when done for all the child components, makes the following layout.

![[Pasted image 20231104194928.png|350]]