A few of the less used operators in JavaScript are **spread** operator and **rest** operator.

### Spread Operator
Printing out the names of hundreds of students stored in an array or an object is quite tedious. The fast way is the **spread** operator `...`
```js
const students = ["John", "Mary", "Isiaha", "Ali", "Michael"];

console.log(...students);
```

### Rest Operator
It is used in creating sub-arrays out of lengthier arrays.
```js
// Creating an array
const students = ["John", "Mary", "Isiaha", "Ali", "Michael"];

// The first three variables are assigned to the first three elements and the rest of the elements are pushed in the participants array
const [john, mary, isiaha, ...participants] = students;

console.log(john, mary, isiaha);
console.log(participants);
console.log(students);
```

<br>

>[!info] De-structuring
>In the above code, the `students` array is de-structured or in other words, it is broken down into several components.
>```js
>const toppers = ["Isiaha", "Michael", "Mary", "John", "Ali"];
>const [first, second, third, …consolation] = toppers;
>
>console.log(first);
>console.log(consolation);
>```  
>Each of the variables `first`, `second` and `third` have the values as the first three elements of the array and the rest are stored in the `consolation` array.

^4911b4


