A sequence of alphabetical characters is called a **string**. In simpler terms, text is of **string** data type. ^28e4c8
```js
/*Here we assign a string ("John") to a variable*/
var name = "John";

/*This statement prints the data type of the value of the variable.*/
console.log(typeof(name));
```

### Syntax
**Strings** must be enclosed within **single-quotes** `''` or **double-quotes** `""`.
```js
/*Below is a string*/
console.log("I am a Human");

/*This is the same as above*/
console.log('I am a Human');
```

```js
/*Below is an exception*/
console.log('It's sunny today');
```

>[!Note]
>The error above occurred because the symbol for apostrophe and single-quotes is the same.
>Thus, the compiler treats the apostrophe as the end of the statement,  `'It'` in this case.
>A better practice is to use **double-quotes** for **strings**.
>```js
/*Below is an exception*/
console.log("It's sunny today");

<br>

### Concatenation
It basically means to join or adhere. In the context of **strings**, it means to join two or more strings into one using the [[Operators#Arithmetic Operators|addition operator]]. ^635605

```js
/*Declaring two variables and assigning them a string*/
var string1 = "Hello"
var string2 = "World"

/*This is what "concatenating two strings" mean*/
var greeting = string1 + string2

console.log(greeting)
```

>[!info] Empty Strings
>Strings with no value, generally used as placeholders.
>```js
>var name = "";
>console.log(name);
>```