**Recursion** means *repeating an action*, just like loops. But, recursion can also be achieved using functions.

### Approach
Say you have to make a counter of $n$ days in the console. 

* ##### Using Loops
A `for` loop would do the work.
```js
// Sample variable to test the loop
var n = 5;

// The loop
for (var i = n; i >= 1; i--) {
	console.log("Day", i);
}
```

<br>

* ##### Using Functions
Herein, we call the function inside itself.

```js
// The function
function getDays(n) {
	console.log("Day", n);
	if (n === 1) {
		return;
	} else {
		getDays(n - 1)
	}
}

// Sample call to test the program
getDays(5);
```

On running the program, 
* First, `Day 5` is printed.
* If the value of `n` is `1`, exit the function and terminate the program else call `getDays(n - 1)`.
* The function `getDays()` then gets called for `n - 1 = 5 - 1 = 4`.
* The above steps are repeated until `n === 1`. 

> [!note] 
> The bottom limit for `n` was chosen to be `1` as the function would be called for `n - 1` which would be `0` in the case, printing `Day 0` which didn't make much sense.

