Now that you have marked the answer sheets as the [[Course/FrontEnd Dev/(2) JavaScript/Module 1/Loops/Concept|examiner]], it's time to declare the result.
You have to print the marks against the name of each candidate.
`Name => Marks` ^48d621

It's code would be 
```js
var name = "Some Name";
var result = 70

console.log(name, "=>", result)
```

To write this over and over again for different names, numerous variables would have to be declared. Thus, we use **functions**.
Re-usable pieces of code which perform a given *function* are called **functions**.

### Syntax
```js
//Defining a function
function functionName(parameter1, parameter2) {
	//Code Block
}

//Calling the function
functionName(argument1, argument2);
```

| Component | What it means |
|--|--|
| `function` | It indicates that the following code is a function |
| `functionName()` | Name of the function |
| `parameter1`, `parameter2` | **Parameter** is the variable that acts as a placeholder. There can be multiple **parameters** |
| `Code Block` | This is the body of the function. It tells the computer what to do |
| `argument1`, `argument2` | **Argument** is the input given to the function while calling it. It is also the value of the **parameter** |

### Application
The function `result` for printing the result in the given format would be the following.
```js
function result(name, marks) {
	console.log(name, "=>", marks);
}

result("John", 80);
result("Mary", 65);
result("Isiaha", 90);
```

>[!note]
>The same parameter name must be used throughout the function for the same parameter.
