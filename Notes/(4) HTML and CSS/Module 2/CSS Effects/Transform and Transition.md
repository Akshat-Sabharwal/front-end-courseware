First, the change to be made is defined. Then the duration and other properties are specified.

##### Properties
This method involves two properties.

* ##### Transform
It is a CSS property that is used to *alter* or *change* an HTML element's appearance.

  Some common functions to change the appearance using `transform`,

  | Function | What it does | Example |
|--|--|--|
| `scale()` | Increase or decrease the size of a component | `transform: scale(2);` |
| `skew()` | Tilt a component | `transform: skew(20deg);` |
| `rotate()` | Rotates a component | `transform: rotate(90deg);` |

  ###### Example
  For instance,
  ```css
.box {
	transform: scale(1.5);
}
  ```
  This would make the box $1.5$ times bigger than its original size. 

<br>

* ##### Transition
  It is also a CSS property and it describes *the **how** of an animation*. 
  The basic value it accepts is of the **duration** of the animation.

  ###### Example
  For instance,
  ```css
.box {
	transform: scale(1.5);
	transition: 0.5s;
}
  ```
  This would create an animation of the box getting $1.5$ times bigger than its original size.
