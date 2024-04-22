Such properties define how the components occupy the space inside the flexbox.

### Flex-Wrap
Determines if the contents of the flexbox occupy another line when needed or get squished. It can have the following values.

| Value | What it does | Visual Depiction |
|--|--|--|
| `wrap` | Uses another line if the contents cannot fit in a single line | ![[Pasted image 20231103133305.png\|200]] |
| `nowrap` | Squishes the components but doesn't occupy another line | ![[Pasted image 20231103133421.png\|200]] |


### Flex-Grow
Determines how much of the available space the child components will acquire. It's value is a ratio which can be any number. When set to a specific child component, it occupies more space than the others.

##### Example
* `.container {flex-grow: 0;}`
The children do not occupy the excess space.
![[Pasted image 20231103134122.png|250]]

* `.container {flex-grow: 1;}`
The children stretch themselves to occupy equal space.
![[Pasted image 20231103134316.png|250]]

* `.child {flex-grow: 0.5;}`
The child component grows $0.5$ times less than the other one.
![[Pasted image 20231103134608.png|250]]

### Flex-Shrink
Same functionality as `flex-grow`. The difference is that it specifies the rate at which the components shrink on decreasing the viewport size.

##### Example
* `.container {flex-shrink: 0;}`
If the content width is more than that of the flexbox, the contents will start ***overflowing***.

![[Pasted image 20231103140717.png|250]]
* `.container {flex-shrink: 1;}`
Each box would **shrink** or get squished, equally, to fit into the flexbox.
![[Pasted image 20231103140914.png|250]]

* `.child1 {flex-shrink: 3;}`
The first child component will shrink $3$ times more than others.
![[Pasted image 20231103141815.png|250]]

### Flex-Basis
It is **like** the width of the child components but not exactly the width. It can have the following values.

| Value | What it does | Visual Depiction |
|--|--|--|
| `content` | Checks for the width of the contents of the child component and sets the value such that they fit inside, properly | ![[Pasted image 20231103142624.png\|200]] |
| `auto` | If the width is not specified, uses `content`; else, the width specified in the `width` property | ![[Pasted image 20231103142624.png\|200]] |
| Any numerical value | Sets the width of the component | ![[Pasted image 20231103143516.png\|200]] |

<br>


> [!info] 
> #### `width` *vs* `flex-basis`
When `flex-basis: 0;`, the component will have the minimum size such that the contents inside the child component fit completely.
![[Pasted image 20231103143759.png|250]]
Whereas, in the case of width, the child component completely collapses.
![[Pasted image 20231103143859.png|250]]

<br>

### Flex-Flow
Specifies the direction of the flexbox. There can be two directions.

* ##### Row 
Left-right direction 
![[Pasted image 20231031143606.png\|250]]  
* ##### Column
Top-bottom direction 
![[Pasted image 20231031143758.png\|250]]


