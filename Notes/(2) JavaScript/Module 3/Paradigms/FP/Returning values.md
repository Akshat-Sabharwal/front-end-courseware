A function for calculating the speed of a car would be 
```js
function getSpeed(distance, time) {
	console.log(distance / time);
}
```

What about acceleration?
```js
function getAcceleration(speed, time) {
	console.log(speed / time);
}
```

But, the speed is calculated by another function `getSpeed()`. The result of the `getSpeed()` function can be used as an input in the `getAcceleration()` function using **`return` statements**.

```js
// Defining the functions
function getSpeed(distance, time) {
	return distance / time;
}

function getAcceleration(speed, time) {
	return speed / time;
}

// Declaring the variables
var sampleDistance = 100;
var sampleTime = 2;

// Assigning the returned values to variables
var calaculatedSpeed = getSpeed(sampleDistance, sampleTime);
var acceleration = getAcceleration(calaculatedSpeed, sampleTime);

// Printing the values in the console
console.log(calaculatedSpeed, acceleration);
```

Here, the `return` statement gives back the output whenever the function is called.
