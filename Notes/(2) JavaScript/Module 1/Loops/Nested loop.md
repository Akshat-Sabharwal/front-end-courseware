A loop in another loop is called a **nested loop**. 

### Syntax
It is essentially made up of the `for` loops and `while` loops. Therefore, there is no different syntax for nested loops. In the each iteration of the outer loop, the inner loop completes all of its iterations. 

```js
for (expression1) {
		//Code block
		for (expression2) {
			//Code Block
		}
}
```

### Example
Say you have to print the days of two consecutive weeks. 
```js
for (var i = 1; i <= 2; i++) {
	console.log("Week", i)
	
	for (var k = 1; k <= 7; k++) {
		console.log("Day", k)
	}
	
}
```

* On running the code, when `i = 1`, `Week 1` will be printed
* Then the inner loop will be completed.
* The second iteration of the outer loop starts at `i = 2` 
* The complete inner loop is executed.