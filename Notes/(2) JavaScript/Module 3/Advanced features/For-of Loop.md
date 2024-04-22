Say, an object has been created with some transactions in it.

```js
const transactions = {
	John: -100,
	Mary: +30,
	Isiaha: +170,
	Ali: -80
}
```

In order to list all the transactions, the following program would have to be used.
```js
console.log(transactions.John);
console.log(transactions.Mary);
console.log(transactions.Isiaha);
console.log(transactions.Ali);
```

### Syntax
```js
for (item of iterable) {
	// Code Block
}
```

| Component | What it means |
|--|--|
| `for` | Indicates a `for` loop |
| `item` | Variable that iterates over |
| `iterable` | An *iterable* object or an object that can be iterated over |

### Example
Here, we need to iterate over the values of the `transaction` object. We thus use the `values()` method of the `Object` constructor.
```js
const transactions = {
	John: -100,
	Mary: +30,
	Isiaha: +170,
	Ali: -80
}

for (person of Object.values(transactions)) {
	console.log(person);
}
```

