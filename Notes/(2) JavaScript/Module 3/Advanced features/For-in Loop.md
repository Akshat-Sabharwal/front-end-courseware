Similar to the [[For-of Loop|for-of loop]], it is used to iterate over JavaScript components. The difference is that `for-of` loop is better suited for iterable objects like *arrays* and the `for-in` loop is suitable for objects.

### Why?
Using a `for-of` loop and a `for-in` loop on a `car` object and an [[Arrays|array]], gives the following result.

* #### On Object
```js
const car = {
	speed: "slow",
	weight: 1000
}

for (let property in car) {
	console.log(property);
}

for (let property of car) {
	console.log(property);
}
```

| `for-of` | `for-in` |
|--|--|
| Returns the [[Objects#^4eabae\|keys]] of the object | raises `TypeError()` saying `car object is not iterable`  |

<br>

* #### On Arrays
```js
const parts = ["engine", "chassis", "battery"];

for (part of parts) {
	console.log(part);
}

for (part in parts) {
	console.log(part);
}
```

| `for-of` | `for-in` |
|--|--|
| Yields the elements of the array | Returns the indexes of those elements |
Thus, the `for-of` loop is better for iterable components.