In JavaScript, we create **conditionals** using the `if` and `else` statements.
### Syntax
Here, `condition` is replaced with the condition to be met. If the statement is true, `Event 1` is executed. Otherwise, `Event 2` will be executed.
```js
if (condition) {
	Event 1
} else {
	Event 2
}
```

### Example
Taking up the previous example of the examiner, we can write a JS code for it.
```js
/*Arbitrary marks for testing the program*/
var marks = 80

/*If marks are greater than 40, print "Pass" in the console.*/
if (marks > 40) {
	console.log("Pass")
} 

/*Otherwise, print "Fail"*/
else {
	console.log("Fail")
}
```
##### Multiple Conditions
Often, multiple conditions are to be met. For instance, only an adult of the Indian nationality can participate in the General Elections. 

In such cases, we can use any of the below.
* `||` or `&&` logical operators
* `and` or `or` keywords

```js
var age = 26
var nationality = "Canadian"

if (age > 18 && nationality == "Indian") {
	console.log("Eligible to vote")
} else {
	console.log("Not eligible to vote")
}
```

##### Multiple Cases
Say you are a data analyst and have to sort out the *Children*, *Adult* and *Senior Citizen* based on their age.
Here, we use the `else if` statements to support multiple cases.

```js
var age = 56

if (age < 18) {
	console.log("Child")
} else if (age > 18 && age < 60) {
	console.log("Adult")
} else {
	console.log("Senior Citizen")
}
```

>[!Note]
>The `else if` statement can be used multiple times in a conditional but the `if` and `else` statements must be used only once, each.