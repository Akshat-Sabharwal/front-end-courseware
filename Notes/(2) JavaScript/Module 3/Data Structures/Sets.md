They basically are arrays with the only difference being that **sets** cannot contain duplicate elements.

### Syntax
```js
var array = [1, 2, 3, 4,];

const sampleSet = new Set(array);
```

| Component | What it means |
|--|--|
| `sampleSet` | Name of the set |
| `new` | To create a new instance of the object `Set()` |
| `Set()` | Constructor function of the `Set()` object |
| `array` | A sample array that the `Set()` constructor takes in as an argument |

Initially, there isn't much use of **sets**. Thus, extra methods aren't mentioned here.
### Example
Repeating items in a grocery list would neither be nice to the pocket nor to the storage.
```js
let groceryList = ["milk", "oatmeal", "bread", "eggs", "cereal", "milk"];

groceryList = new Set(groceryList);
console.log(groceryList)
```
Here, the repeated item `milk` has been removed as **sets** can not contain duplicates.