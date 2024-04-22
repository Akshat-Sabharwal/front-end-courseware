Such properties define how the components are **positioned relative to the flexbox** or simply, inside the flexbox. 

### Justify-Content
It is used to *align* or *position* items along the main-axis. It can have the following possible values.


| Value | What it means | Visual Depiction |
|--|--|--|
| `flex-start` | All the components aligned to left | ![[Pasted image 20231031155125.png\|200]] |
| `flex-end` | All the components aligned to right or bottom | ![[Pasted image 20231031154852.png\|200]] |
| `center` | Aligned to the center | ![[Pasted image 20231031154916.png\|200]] |
| `space-between` | Space between the elements but not between them and the edges | ![[Pasted image 20231031154955.png\|200]] |
| `space-evenly` | Equal space between the elements and the edges | ![[Pasted image 20231031155034.png\|200]] |

<br>

### Align-Items
It positions the child components on the cross-axis.

| Value | What it means | Visual Depiction |
|--|--|--|
| `flex-start` | Places the components along the starting edge, top or left | ![[Pasted image 20231031160029.png\|200]] |
| `flex-end` | Places the components along the starting edge, bottom or right | ![[Pasted image 20231031160101.png\|200]] |
| `center` | Children aligned to the center | ![[Pasted image 20231031160145.png\|200]] |
| `baseline` | Placed next to each other with their **baseline** or bottom edge aligned | ![[Pasted image 20231031204211.png\|200]] |
| `stretch` | Makes the children occupy the space across the cross axis evenly | ![[Pasted image 20231031212325.png\|200]] |

<br>

### Align-Self
It is used on the child component to position it uniquely along the cross-axis. There is no need for the main-axis, thus, `align-self` doesn't exist for the main-axis.

<br>

| Value | What it means | Visual Depiction |
|--|--|--|
| `flex-start` | Places the child component along the starting edge, top in the case of row or left in the case of column | ![[Pasted image 20231103132037.png\|200]] |
| `flex-end` | Places the child component along the ending edge, bottom or right | ![[Pasted image 20231103132515.png\|200]] |
| `center` | Aligned along the center | ![[Pasted image 20231103132546.png\|200]] |
| `baseline` | Placed next to other components with their **baseline** or bottom edge aligned | ![[Pasted image 20231103132613.png\|200]] |
| `stretch` | Makes the child component occupy the space across the cross axis evenly | ![[Pasted image 20231103132613.png\|200]] |


