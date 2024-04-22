We had created [[Objects|objects]] for the employees for efficient management. But creating hundreds of such objects would still be repetitive.

Also, notice that the properties and methods are the same for every employee, just the values differ. We, can, thus, create a framework of an **Employee** called **class** with the following properties and methods.

<iframe style="border: 1px solid rgba(0, 0, 0, 0.1);" width="800" height="450" src="https://www.figma.com/embed?embed_host=share&url=https%3A%2F%2Fwww.figma.com%2Ffile%2FBG0ctO2Yn2nLYzh69FixEY%2FClasses%3Ftype%3Dwhiteboard%26node-id%3D0%253A1%26t%3DS4cu1wDk9whc38t1-1" allowfullscreen></iframe>
^906559

Each employee would thereby be called as an **instance** of the **class** Employee and *instantiating the class* would mean the creation of an employee.

### Syntax
Below is a **class** named `className` with two methods `constructor` and `method1`. 
```js
class className {
	constructor(argument1, argument2) {
		this.property1 = argument1;
		this.property2 = argument2;
	}
	method1() {
		// Code Block
	}
}
```

| Component | What it means |
|--|--|
| `class` | It is the keyword to make a class |
| `className` | Name of the class |
| `constructor` | A special method which is automatically called at the time of instantiation |
| `this.property1` | Referring to `property1` of the instance |
| `argument1` | The value assigned to `property1` |

<br>

The method named `constructor` is a special type of method called **constructor**.  It is called as soon as a class is *instantiated* or *an instance of the class is created*. It isn't required to call.

```js
// Instantiating the class
const instance = new className();

// Calling a method of the class instance
instance.method1();;
```


### Example

* ##### Employee
A class named **Employee** can be created, similarly. An instance of the class `Employee` is an **object**, itself. Here `john` is an object.
```js
// A basic framework for Employee
class Employee {

	// A function called at the time of instantiation
	constructor(name, id, designation, job) {
	
		// All the properties (data) of an employee
		this.name = name;
		this.id = id;
		this.designation = designation;
		this.job = job;
	}
	
	// A method which prints the job of the employee
	work() {
		console.log(this.job);
	}
}

// Instantiating the Employee class
const john = new Employee("John", 1001, "Manager", "Supervise and lead the team");

console.log(john);
```

<br>

* ##### Animal
Animal can be treated as a class which can have many different instances such as dogs and cats. ^57f14e
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

// Instantiating or creating an instance of the class
const dog = new Animal("Dog", "woof", "Black");
const cat = new Animal("Cat", "meow", "Snowwhite");

dog.makeSound();
cat.makeSound();
```

^b634f5

