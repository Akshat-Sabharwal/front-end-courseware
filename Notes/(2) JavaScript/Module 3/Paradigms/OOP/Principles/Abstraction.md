The procedure of simplifying and generalizing things is called **abstraction**. 

In the example of [[Inheritance#Example|animals]], the `Animal` class is not used or *instantiated* directly instead it forms the super-class of `Fish` and `Bird` classes. Here, `Animal` is an **abstract class**. The methods of such classes are, therefore, **abstract methods**.

### Example
`Shape` forms the base-class of `Triangle` because triangle is a form of shape. Here, `area` is an abstract method as the dimensions of the shape are not accepted in the `Shape` class but it still has some unknown area.

```js
// Abstract class
class Shape {
	constructor(sides) {
		this.sides = sides;
	}
	// Abstract method
	area() {
		console.log("Dimensions not known!")
	}
}

// Concrete class
class Triangle extends Shape {
	constructor(height, base, sides = 3) {
		super(sides);
		this.h = height;
		this.b = base;
	}
	area() {
		return (this.h * this.b * 0.5)
	}
}

const triangle = new Triangle(5, 5);
console.log(triangle.area());
```