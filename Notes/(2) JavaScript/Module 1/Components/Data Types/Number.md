Simply put, **number** data type contains integers and decimals of a certain range.
```js
/*Data type*/
console.log(typeof(100))

/*When enclosed in quotation marks, numbers are treated as strings*/
console.log(typeof("100"))
```

### Syntax
Numbers do not need any extra add-ons. 
```js
console.log(198)

console.log(3.14)

console.log(-1/2)

console.log(8 % 3)
```

### Concatenation
Numbers do **concatenate** with numbers only if even one of the is a **string**.
```js
var a = "10"
var b = 20

console.log(a + b)
```

Numbers **concatenate** with strings, too.
```js
var name = "John"
var age = 32

console.log(name + age)
```