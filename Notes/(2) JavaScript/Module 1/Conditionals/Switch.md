As an alternative to the [[If...else|if-else]] statement, **switch** statement can be used.

### Syntax
Just as in **if-else** statements the **conditionals** act as a trigger point to an event, **cases** act as the trigger points to those events in **switch** statements.

Here, `expression` is replaced with the parameter that might have many values.

If the value of the `expression` is `value1`, `event1` will take place. If the value is `value2`, `event2` will take place and so on. 
If no case matches the value of the expression, the default case will be executed.
```js
switch(expression) {
	case value1:
		event1;
		break;
	
	case value2:
		event2
		break;
		
	default:
		event0;
}
```

The code above when programmed in `if-else` statements would be the understated.  
```js
if (expression === value1) {
	event1;
} else if (expression === value2) {
	event2;
} else {
	event0
}
```


### Example
You are a Software Engineer in an automotive company. You have been assigned the project to display on the car's dashboard screen, when to move, stop or halt, given the state of traffic light.

```js
/*For testing the program*/
var light = "green"

/*The variable "light" can have many possible cases, so it is the expression*/
switch(light) {
	/*When `light = "green"`, "You can go" will be printed*/
	case "green":
		console.log("You can go");
		break;
		
	case "red":
		console.log("Stop!");
		break;
		
	case "yellow":
		console.log("Halt");
		break;
		
	default:
		break;
}
```