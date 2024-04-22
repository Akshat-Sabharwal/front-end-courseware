Say, for instance, you have been given a list of book titles. 
```js
const bookTitles = ["The Alchemist", "Karma", "The Hobbit", "Sapiens"];
```

The task is to create a `Book` instance of each of the list elements.
```js
class Book {
	constructor(title) {
		this.title = title;
	}
}
```

One way would be to do it all, one-by-one.
```jsx
const hobbit = new Book("The Hobbit");
const karma = new Book("Karma");
const alchemist = new Book("The Alchemist");
const sapiens = new Book("Sapiens");
```

The other, effective, way is to use the `map()` method.

### Mapping
`map()` is a method in JavaScript to ***transform*** elements of a JS list to other components.

##### Application
It basically says, * **map** or **transform** each item in the list to `objectTochangeTo` and store  the new list in `mappedList`.*
```js
const someList = ["element1", "element2", "element3", "element4"];

const mappedList = someList.map(item => { return objectToChangeTo })
```
<br>

##### Example
Implementing the above example, programmatically,

```js
class Book {
	constructor(title) {
		this.title = title;
	}
}

const bookTitles = ["The Alchemist", "Karma", "The Hobbit", "Sapiens"];

const books = bookTitles.map(bookTitle => { 
		let bookInstance = new Book(bookTitle);
		return bookInstance; 
});

console.log(books);
```

<br>

>[!tip]
>This transformation or ***mapping*** can be done for lists of React components as well.
>

<br>

### Filtering
Another tool for list transformation which ***filters*** or *excludes elements from lists that do not meet a certain condition*. 

##### Application
This is done using the `filter()` method on lists. 

It basically says, *filter all the items in the list which do not meet `condition`.* If the `condition` is true, the item will be kept else, excluded.
```js
someList.filter((someItem) => {
	return condition;
})
```


##### Example
To filter out all the books which contain “the” in their title, the following code can be used.
```js
bookList.filter((book) => {
	let pattern = new RegExp("the");
	return pattern.test(book.title());
})
```

<br>

### Sorting
To ***sort** a list* means to *arrange the list items in a specific order*. 

##### Application
This can be done using the `sort()` method on the lists with a function, called the **compare function**, as its argument.

```js
someList.sort((item1, item2) => {
	item1 - item2;
});
```


##### Example
Sorting the book list in alphabetical order, doesn’t require a **compare function**. 
```js
bookList.sort();
```