The term itself, Object-Oriented programming or **OOP** for short, means *programming with a profound use of [[Objects|objects]]*.  

Herein, data with similar properties is grouped under an object, unlike **FP**.

### Example
Writing [[Course/FrontEnd Dev/(2) JavaScript/Module 3/Paradigms/FP/Concept#Example|this]] program in OOP paradigm,
```js
// The object with all the data of the transaction
var transaction = {
	// Properties
	cost: 100,
	taxRate: 3,
	// Method
	totalPrice: function() {
		return transaction.cost + (transaction.cost * transaction.taxRate / 100)
	}
}

// Calling the method totalPrice()
console.log(transaction.totalPrice());
```
