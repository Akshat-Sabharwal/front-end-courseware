In the [[Course/FrontEnd Dev/(2) JavaScript/Module 3/Paradigms/FP/Scope/Concept#^956532|scenario]] of a school, the students of *Class A* can be accessed only by *Teacher A* and same for *Class B*. Thus, the students of *Class A* belong to the **local scope** for *Teacher A*.


Variables in the **local scope** are *localized* or can be accessed only in the part of the program where it is declared.

```js
fucntion declareName() {
	var name = "John";
}

console.log(name);
```
Here, the compiler *throws* the `Unexpected Identifier` error because `name` is in the **local scope** and can only be accessed within the function.
<br>

> [!note]
> The name has been printed outside the function
