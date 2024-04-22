There are many testing frameworks available for JavaScript. **Jest** is one of them. Writing tests for code using Jest is efficient as it supports **Code Coverage** which is the percentage of code covered in tests.

### Setup 
First, the Jest package is to be installed using **npm**.
```CLI
npm install jest
```

A test file is created separately for testing. 
```js
// main.test.js

// The default framework to run the tests would be Jest and thus, it is required in this file
const {default: TestRunner} = require("jest-runner");

// The function add() is to be tested and has to be imported from main.js file
const {add} = require('./main.js');
```

A main file where a function to be tested is stored.
```js
// main.js
function add(a, b) {
	return a + b;
}

module.exports = {add};
```
The `module.exports = {add}` means that *the following objects or functions can be accessed by other files*.

The test is created using the `test()` method.
```js
// main.test.js

const {default: TestRunner} = require("jest-runner");
const {add} = require('./main.js');

// test() takes two arguments
// 1. A comment
// 2. A function or rather the test itself

test('Adds two numbers', () => {
	// Expect the value that this function returns to be 3. If not, the test fails. 
	expect(add(1, 2)).toBe(3);
})
```


