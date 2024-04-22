Simply put, it is the ***measure of amount of resources required to complete an operation***. It is important as the code written should be as efficient as possible.

### Time Complexity
The **time complexity** of a piece of code is denoted by what’s called, the **Big-O notation** or **O**. The time complexity depends on the code and data used.


* ##### Constant Time Complexity
As the name conveys, the time taken for such processes is constant, regardless of the data or other factors.

  For instance, to print the 5th item in the list, 
  ```js
const array = [1, 2, 3, 4, 5];
console.log(array[4]);
  ```
  In the code above, even if the list contains 100 items, only the 5th item will be accessed. This code is said to have **constant time complexity**.

  ![[Pasted image 20231128181905.png|200]]

  Constant Time Complexity is represented by **O(1)**.

<br><br>

* ##### Linear Time Complexity
It, basically, means that the task to be done depends on *how big the data is*. It, generally, is in the case of single loops.

  For instance, to print each item in the list, the list must be iterated over.  
  ```js
const array = [1, 2, 3, 4, 5];
for (item of array) {
	console.log(item);
}
  ```
  The time complexity, here, depends on the number of items the list contains. If it was 10 instead of 5, the time taken would be double than in the case of 5 items.

  ![[Pasted image 20231128183218.png|300]]

  Linear Time Complexity is represented by **O(n)**.

<br><br>

* ##### Quadratic Time Complexity
It is one of the highest time complexities and this shouldn’t be the case in any code. In such a case, if the input size is $n$, the time complexity would be $n^2$. 

  For instance, the nested loop below will print every possible pair of items in the array.
  
  ```js
const array = [1, 2, 3, 4, 5];
for (item1 of array) {
	for (item2 of array) {
		console.log(`(${item1}, ${item2})`);
	}
}
  ```
  This means that a loop would be executed for every item in the list. So, if an item is added, an extra loop would have to be executed.

  ![[Pasted image 20231128185034.png|200]]

  Quadratic Time Complexity is represented by **O($n^2$)**.

<br>

### Space Complexity
The concept of **space complexity** is just the same as that of **time complexity**, the difference being that instead of **time**, it measures the ***memory required by the operation*** or **space**.




