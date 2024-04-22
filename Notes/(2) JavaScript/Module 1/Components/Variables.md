Placeholders to store data. The term **variable** itself refers to something which can change.

## Syntax
```js
/*To declare a variable and assign it a value*/
var name = "John";
```

| Component | What it means |
|--|--|
| `var` | It is a **keyword** that declares a variable |
| `name` | Name of the variable |
| `=` | Assignment operator |
| `"John"` | Value of the variable |
| `;` | End of line of code |


## Usage
Variables are generally used when the data to store is unknown or is bound to change.
* ##### Input
In the case of inputs, we do not know the value beforehand and thus, variables are used.
<br>
* ##### Repetition
Often, a value is to be used several times in a code and variables make the code cleaner.



## Example
```js
/*Declare a variable*/
var marks = 90;

/*Print "Your Grade: 90" in the console*/
console.log("Your Grade: ", marks);

/*Updating the value of the variable*/
marks = 94;

/*Print "Your Grade: 94" in the console*/
console.log("Your Grade: ", marks);

```

In the above example, the variable `marks`, initially, is assigned a value of `90`. Later, its value is updated to `94`. 

> [!Note]
>`var` keyword isn't used while updating the value of 
>an already declared variable.

