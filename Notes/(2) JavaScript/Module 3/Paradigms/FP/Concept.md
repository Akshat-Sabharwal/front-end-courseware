**FP** for short, functional programming majorly involves **functions** to write programs. The variables are separated from the functions, herein. 

### Example
A program, in the FP paradigm, for calculating the total price of a transaction.

```js
// Function separated from the data
function totalPrice(cost, taxRate) {
	return cost + cost * taxRate / 100
}

// Data in the form of variables
var sampleCost = 100;
var sampleTaxrate = 3;

// Invoking the function with the data 
var amount = totalPrice(sampleCost, sampleTaxrate);
console.log(amount);
```
