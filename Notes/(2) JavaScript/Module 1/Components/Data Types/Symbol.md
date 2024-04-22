Generally used in **cryptography**, symbols are unique objects that are used in identifying other objects.
For instance, your fingerprint or your DNA is a **symbol** to you and this **symbol is never same**.

### Syntax
It can be used by calling the **Symbol()** function.

```js
var id = Symbol("MachoMan")

console.log(id)
console.log(typeof(id))
```

### Working
Symbols are randomly generated. They are not dependent on the content.
As an example, many companies have employees with the same name. To differentiate them, we assign them an **Employee ID** that is different for every employee. 
```js
/*Generating Employee IDs (symbols) of the same name "Harry"*/
var id1 = Symbol("Harry")
var id2 = Symbol("Harry")

/*Despite of the symbols with the same content, the symbols are not same, they are unique*/
console.log(id1 == id2)
```
