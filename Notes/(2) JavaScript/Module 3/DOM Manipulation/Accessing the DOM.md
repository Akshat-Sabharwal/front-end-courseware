DOM or [[DOM|Document Object Model]] can be accessed using JavaScript in the browser. 

#### `document` Object
Each webpage is stored in a DOM, and precisely, inside a JavaScript object named `document` which can be accessed through the console as follows.

```js
document
```

### Creating Elements
Elements can be created using JavaScript, as well.
```js
document.createElement('h1');
```
This creates an `<h1>` element in the webpage.

### Accessing Elements
The elements inside the `document` object  can be accessed by using the `querySelector()` method which takes in the element as an argument.

```js
// This will return the first <h2> element
document.querySelector("h2");
```

These elements can be accessed by `class` and `id` as well.
* ##### `class`
This can be done using the `getElementbyClassName()` method.
```js
document.getElementbyClassName("primary");
```

* #### `id`
This can be done using the `getElementbyId()` method.
```js
document.getElementbyId("heading");
```


### Editing the Elements
Just accessing and not being able to edit these elements would be meaningless. This can be achieved using the `innerText()` or `innerHtml()` methods.

```js
const heading = document.querySelector('h1');
heading.innerText = "Hello World!";
```

This changes the text of the heading to `Hello World!`.