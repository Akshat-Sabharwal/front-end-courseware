The act of taking possession from previous generations is called **inheritance**. For instance, a child inherits his/her ancestral property.

In the example of [[Classes#^b634f5|animals]], knowing that animals can have numerous sub-categories such as mammals, birds, fishes, amphibians, etc. **Sub-classes** for the can be created, as well.

<iframe style="border: 1px solid rgba(0, 0, 0, 0.1);" width="800" height="450" src="https://www.figma.com/embed?embed_host=share&url=https%3A%2F%2Fwww.figma.com%2Ffile%2FnGPOgoh1QTJOISX6lfGx0N%2FUntitled%3Ftype%3Dwhiteboard%26node-id%3D0%253A1%26t%3D5CzRgvcOJtOfsbJm-1" allowfullscreen></iframe>

The two **sub-classes**, Birds and Fishes, have a common parent class, also called the **super-class**, Animal.

### Syntax
The `extend` keyword is used to indicate inheritance. The `super` keyword instructs which argument is to be inherited.   
```js
class subClass extends superClass { 
	constructor(arg1, arg2) {
		super(arg2);
		this.param2 = arg2;
	}
	
	method1() { /*Code Block*/ }
	
	method2() { /*Code Block*/ }
}
```


### Example

^ed0efa

```js
// Animal Class
class Animal {
	constructor(type, sound, color) {
		this.type = type;
		this.color = color;
		this.sound = sound;
	}
	makeSound() {
		console.log(this.sound);
	}
}

// Fish Class
class Fish extends Animal {
	constructor(color, habitat) {
		super(color);
		this.habitat = habitat;
	}
	move() {
		console.log("Swimming in the waters!");
	}
}

// Bird Class
class Bird extends Animal {
	constructor(color, habitat, sound) {
		super(color, sound);
		this.habitat = habitat;
	}
	move() {
		console.log("Cutting through the air!")
	}
}

var sparrow = new Bird("brown", "forest", "chirp");
var dolphin = new Fish("black-white", "oceans");

sparrow.makeSound();
dolphin.move();
```

^90af74

> [!note]
> We didn't write the `makeSound()` method for the `Bird` class but it was successfully called, for the `Bird` class inherits the methods of `Animal` class, as well.
> 
