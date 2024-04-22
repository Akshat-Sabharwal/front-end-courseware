Say, you are assigned to build a webpage which displays the price of a car from another website.


![[Pasted image 20231123170711.png|300]]


Manually, updating the value of a state variable will be not be effective. Instead, something which would automatically get the data and update the state variable would do the work.

This is what’s called ***fetching***. *Fetch* means *to get*. Thus, ***fetching** data* means *getting data from another source*.


### Approach
For this, JavaScript has a special **Browser [[Basic Concepts#API|API]]** called `fetch()`. The `fetch()` function takes a URL as an argument. When `fetch()` is invoked, the data at the URL is brought into the web app. 


![[Pasted image 20231123175620.png|600]]

Then, this data is converted into **JSON**. Then, it is stored in the state variable of the Car price.
Both these actions are done at the time of arrival of data using `then`.

>[!info] JSON
>Standing for **JavaScript Object Identifier**, it is a data format used to store data. It occupies very little storage and is the most efficient form of data storage.
>
>An example of a JSON object storing the Car price would be,
>```json
>”car”: {
>	“carPrice”: 25000,
>}
>```

<br>

### Example
The code for the above example would be,

```jsx
import { useState } from "react";

function App() {
	const [carPrice, setCarPrice] = useState(0);
	
	// Grab the data from the URL, convert it into JSON, update the state variable
	fetch("https://www.thisisnotanactualurl.com/carprice")
	.then((response) => response.json())
	.then((data) => setCarPrice(data.carPrice));
	
	return (
		<p>The Car Price is:</p>
		<h1>{ carPrice }</h1>
	);
}
```