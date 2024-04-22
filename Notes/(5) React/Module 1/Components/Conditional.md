Often, there is a need of a conditionals in webpages. For instance, *if a Boolean variable's  value is **true**, display a heading else not*.

This can be achieved by the standard `if..else` statements. A better way is to use the **Ternary operator**.

### Ternary Operator
Its functionality is the exact same as the `if..else` conditional just with simpler syntax.

##### Syntax
```js
condition ? doThis : doThat
```
It basically says, *is the **condition** true? if yes, **doThis**. else, **doThat** *.

##### Example
To print `Yes, you are right!` if a Boolean variable is true. Else, `No, you are wrong!`.

```js
// Declaring the variable
let isRight = true;

// Using the ternary
isRight === true ? console.log("Yes, you are right!") : console.log("No, you are wrong!")

// Updating the variable
isRight = false;

// Re-using the ternary
isRight === true ? console.log("Yes, you are right!") : console.log("No, you are wrong!")
```
