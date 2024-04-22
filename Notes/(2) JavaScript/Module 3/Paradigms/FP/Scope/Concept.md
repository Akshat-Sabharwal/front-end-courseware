In a school, there are many classrooms which all have a different set of students and a teacher. 
The teacher can deal with the students of his/her own class but not of other classes.
But, the principal must deal with all of the students to keep a check on how well they perform. ^956532

![[Pasted image 20231007231505.png|500]] ^e7cb89
## Why?
Scope might seem unnecessary but is actually very useful.

* Commonly, extra variables have to be declared inside functions which are not significant in the program otherwise, `speed` and `acceleration` in this case. Scope allows for such variables to be inaccessible outside the code.
```js
function getAcceleration(distance, time) {
	var speed = distance / time;
	var acceleration = speed / time;
	return acceleration;
}

console.log(speed);
```

<br>

* Using [[Declaration Keywords|declaration keywords]] other than `var`, makes those variables absolute which can be used to store sensitive information.
```js
// Declaring a variable using const
const name = "John";

// Its value cannot be updated
name = "Mary";
```