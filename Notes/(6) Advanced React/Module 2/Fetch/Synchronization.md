Say, you have planned to plant saplings of *Apple*, *Orange* and *Blueberry*.

![[Pasted image 20231123192224.png|300]]

Planting the sapling of *Apple* and waiting for it to grow and then plant the sapling of *Orange* would make no sense, provided that you have multiple pots and resources.

This is called **synchronous process** which means *to execute the tasks one-by-one*. 

![[Pasted image 20231123191739.png|500]]

This is also called a **single-thread execution** as there is only 1 **thread** which executes all the processes one-by-one.

An effective way would be to plant all of them at the same time. This is called an **asynchronous process** meaning that *the processes are executed are t the same time*.  

![[Pasted image 20231123193236.png|250]]

This is also called **multi-thread execution** as there is one **thread** for each of the saplings.

### Fetching
It is an **asynchronous process**. Meaning that whenever `fetch` is invoked, it is executed in a separate **thread**.

For instance, 
```js
console.log("Before fetching");

fetch("https://www.thisisnotanactualurl.com/somedata")
.then((response) => response.json())
.then((data) => console.log(data));

console.log("Still before fetching");
```
<br>

In the code above, 
* First, `Before fetching` is logged in the console
* Then, `fetch` is invoked
* Simultaneously, `Still before fetching` is logged in the console


![[Pasted image 20231123200600.png|250]]
