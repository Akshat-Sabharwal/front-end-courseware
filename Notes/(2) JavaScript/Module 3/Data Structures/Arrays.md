Containers are used as storage units. Arrays, too, are such containers.

### Syntax
This is the basic structure of an array. Each of the elements has an **index** or the position in the array. `element1` has the index `0`, `element2` has `1` and `element3` has `2`.
```js
var array = [element1, element2, element3];
```

| Component | What it means |
|--|--|
| `array` | Name of the array |
| `[]` | Container |
| `element1, element2, element3` | **Elements** or the data stored in the array |

### Operations 
Just storing data and not being able to retrieve it or edit it would make the container useless. Understated are some of the operation on arrays.
<br>

* ##### Retrieving
Accessing or getting the data back from the array is retrieval. Any element can be accessed if its index is known or vice-versa.
```js
var fruits = ["papaya", "melon", "litchi"];

// Getting the element using index
console.log(fruits[1]);

// Getting the index using the element
console.log(fruits.indexOf("melon"));
```
<br>

* ##### Length
Arrays can contain virtually infinite elements. Knowing the number of elements can be simplified.
```js
var fruits = ["papaya", "melon", "litchi"];

console.log(fruits.length);
```

<br>

* ##### Appending
Adding elements to an array is called **appending**.
```js
var fruits = ["papaya", "melon", "litchi"];

fruits.push("mango");
console.log(fruits);
```


### Example
An array containing some books would be
```js
var books = ["The Alchemist", "The Hobit", "Think and Grow Rich"];
```

```js
// Getting a book
var hobit = books[books.indexOf("The Hobit")]
console.log(hobit);
```

```js
// Adding another book
books.push("Rich Dad Poor Dad");
console.log(books);
```

```js
// Getting the length of the array
var len = books.length;
console.log(len);
```