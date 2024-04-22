The second type of loop in JS is the `while` loop.

### Syntax
Its syntax is somewhat similar to the `if` statement but its components resemble the `for` loop. The `condition` will be replaced by the actual condition. Notice how the [[Course/FrontEnd Dev/(2) JavaScript/Module 1/Loops/Concept#Structure|counter variable]] is declared outside the loop.

```js
var i = 0;

while (condition) {
	//Code block
}
```


### Example
We can construct a `while` loop for the same [[Course/FrontEnd Dev/(2) JavaScript/Module 1/Loops/Concept#Approach|examiner problem]]. 
The above loop will be executed until `k = 100`.

```js
var k = 0

while (k <= 100) {
	if (marks > 40) {
		console.log("Pass")
	} else {
		console.log("Fail")
	}
}
```
