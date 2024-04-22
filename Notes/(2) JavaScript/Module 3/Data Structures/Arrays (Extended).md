A few more methods to manipulate arrays and retrieve the desired data

### `forEach()`
What it says is, *for each element in the array, perform a function*.

Say, you have a list of the students who have passed. The task is to add `Pass` against each of their names. 

One way is using a `for` loop.
```js
const students = ["John", "Isiaha", "Mary"];
const newArray = [];

for (student of students) {
	newArray.push(`${student} : Pass`);
}

console.log(newArray);
```

The other way is `forEach()` method.
```js
const students = ["John", "Isiaha", "Mary"];

// For each student in the array, replace the string at the index with "Name: Pass"
students.forEach(
	function(name) {
		students[students.indexOf(name)] = `${name} : Pass`;
	}
);

console.log(students);
```


### `map()`
It is similar to `forEach()` but the slight difference is that it transforms the array into a new one where `forEach()` performs some action on the same array.

`map()` methods accepts the array, executes the function for each element and stores the result in a new array.
```js
const students = ["John", "Isiaha", "Mary"];

const newStudentArray = students.map(
	function(name) {
		return name + ": Pass";
	}
);

console.log(newStudentArray);
```


### `filter()`
As the name suggests, it *filters* out the unwanted and returns what we input.

```js
const students = ["John", "Mary", "Isiaha"];

const studentsWithNameJohn = students.filter(
	function(name) {
		return name === "John";
	}
)

console.log(studentsWithNameJohn);
```