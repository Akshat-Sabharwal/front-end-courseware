One way of creating variable strings is 
```js
var name = "John"; 
console.log("Hey!", name);
```

But using it for multiple variables isn't much maintainable.

### Syntax
Here, the variable that is to be included in the string, is wrapped inside `{}` *curly-brackets* preceded by a `$` and the string is to be wrapped in `` *backticks*.

```js
var name = "John";

console.log(`Hey! ${name}`);
```