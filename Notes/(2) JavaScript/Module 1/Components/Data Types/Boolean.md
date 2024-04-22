Anything is either **true** or **false**. This represents a **Boolean** data type.

### Syntax
Nothing but the words `true` and `false`, themselves.
```js
/*Assigning the boolean vallue, false, to the variable, attractive*/
var attractive = false

console.log(typeof(attractive));
```

### Logical Operations
Using [[Operators#Logical Operators|logical operators]] on Boolean values, we can manipulate them.
```js
/*I have a dog but I don't have a cat*/
var hasDog = true;
var hasCat = false;

/*I have a pet means I atleast have one of them => OR logical operator*/
console.log("I have a pet:", hasDog || hasCat);

/*I must have both of the pets => AND logical operator*/
console.log("I have both a dog and a cat:", hasDog && hasCat);

/*Opposite of the statement, "I have a dog: true" => NOT logical operator*/
console.log("I don't have a dog:", !hasDog);
```

