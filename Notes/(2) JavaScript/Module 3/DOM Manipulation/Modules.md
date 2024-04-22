One of the ways of writing code professionally and minimizing the effort is using **modules** which basically are pieces of JavaScript code that can be re-used.

Say, for instance, you have been creating a Banking System in JavaScript.
```js
class Bank {
	// A lot of code
}

class Account {
	// Some Code
}

class Savings extends Account {
	// Some code
}

class Current extends Account {
	// Some Code
}
```
In such a case, managing multiple classes in a single file is confusing. These classes can be written and accessed over independent files.

```js
// bank.js

class Bank {
	// Some Code
}
```

```js
// account.js

class Account {
	// Some code
}

class Savings {
	// Some code
}

class Current {
	// Some code
}
```

Each of the files is called a **module**. All of them can be accessed using `import`.

```js
// main.js

import Bank from "./bank.js"
import Account from "./account.js"
```

| Component | What it means |
|--|--|
| `import` | Importing means receiving |
| `Bank, Account` | The classes or methods to import | 
| `./bank.js` | The file which contains the classes or methods |
