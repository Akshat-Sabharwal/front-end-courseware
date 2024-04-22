**Number** data type only deals with numbers in a certain range. The rest is dealt by **BigInt**. It is a **big number** data type, indeed.

### Syntax
It can be assigned in two methods.
* By adding or *appending* an `n` at the end of the number.
* By *calling the function* **BigInt()**.

```js
/*Adding an 'n'*/
var bigNumber1 = 929902948475894003873n
console.log(typeof(bigNumber))

/*Calling the bigint function*/
var bigNumber2 = BigInt(929993874889029837873)
console.log(typeof(bigNumber2))
```