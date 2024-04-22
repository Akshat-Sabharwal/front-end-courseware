Often, while writing and executing code, we face **errors** and **bugs** which prevent the code from running the way we wanted it to.

### Bugs
Mistakes or rather the code, that gets executed in another way which we didn't want.
For instance, 

```js
// Declaring two variables with numbers
var a = 10;
var b = "20";

// Adding the two numbers together
console.log(a + b);
```

Instead of `30`, the result is `"1020"` which is not the desired one. This is a **bug**.


### Error
These are bugs that prevent the code from further execution. For instance,

```js
console.log(c + d);
console.log("Hello World!")
```

Here, the variables `c` and `d` have not been declared, earlier. Thus, it *throws the* **Reference error** and the `Hello World!` statement doesn't get printed as the execution stops.

There are various predefined errors.

| Error | Trigger Point | Example |
|--|--|--|
| Reference Error | Using undeclared variables | `console.log(x + y);` |
| Syntax Error | When the syntax is not correct | `var name = "John;` |
| Type Error | When incorrect methods are used with data types | `var age = 10;` <br> `age.pop();` |


## The Solution
To tackle **errors** and **bugs**, we must first know where they are and then, prevent them from terminating the execution of the code. The `try-catch` statements serve this purpose.

#### Syntax
In the `try` statement, the code block which might produce an error, is placed. If an error is caught, the the code block inside the `catch` statement gets executed.  Here, `err` is the parameter of the `catch` statement which is the error caught.
```js
try {
	//Code Block
} catch(err) {
	//Code Block
}
```

#### Example
The code block inside `try` statement uses an undeclared variable `d` instead of `b`. This must raise the `ReferenceError()` which, in turn, would trigger the code block inside `catch` statement.

```js
try {
	var a = 10;
	var b = 20;
	console.log(a + d);
} catch(err) {
	console.log(err);
	console.log("An error is caught in the above code");
}
```

<br>

Note that there is no error in the code block inside the `try` statement and thus, the `catch` block wouldn't be executed. 
```js
try {
	console.log("Hello World!");
} catch(err) {
	console.log("There was an error");
}
```

<br>

>[!info]
>Often, in high-level programs, there is a need of raising errors, willingly. This can be done using the `throw` statement. 
>```js
>try{
>	throw new SyntaxError()
>} catch(err) {
>	console.log("This error was raised at will")
>}
>```
