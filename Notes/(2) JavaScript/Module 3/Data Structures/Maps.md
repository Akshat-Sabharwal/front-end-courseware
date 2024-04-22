Not the locations ones, they essentially hold data but in a *key-value pair*.

There are 3 boxes each with a label and uniquely colored set of balls.   
![[Pasted image 20231015181503.png|500]]
A simple way to remember the box containing a specific color of balls would be to associate them. 
* Box 1 → Yellow 
* Box 2 → Green
* Box 3 → Pink

This is called a **map** and each of these is called a **key-value pair**.

### Syntax
Here a **map** is created using the `Map()` constructor. 
```js
const colorBalls = new Map();
```

| Component | What it means |
|--|--|
| `colorBalls` | Name of the map |
| `new` | To create a new instance of the object `Map()` |
| `Map()` | Constructor function of the `Map()` object |

### Methods
Some of the methods used on **maps** are as follows.

* #### `set()`
To add a key-value pair
<br>

* #### `get()`
To get the value of a key

### Example
Taking up the instance of box containing balls.
```js
const colorBalls = new Map();

// Adding key-value pairs using set() method
colorBalls.set("Box 1", "Yellow");
colorBalls.set("Box 2", "Green");
colorBalls.set("Box 3", "Pink");

// Retrieving the value of a key
const box2 = colorBalls.get("Box 2");

console.log(colorBalls);
console.log(box2);
```