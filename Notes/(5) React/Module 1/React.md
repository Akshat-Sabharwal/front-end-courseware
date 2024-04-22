Say, as a developer, you are asked to create a *Weather Application* which displays the **current temperature** and the **location**, just like so

![[Pasted image 20231113103902.png|350]]

The HTML code might look like this.

```html
<div id="weather-details">
	<h1>26°C</h1>
	<h4>New Delhi, India</h4>
</div>
```
<br>

Here, the problems kick in. 
* ***The temperature doesn't remain same all the time.***  
* ***Updating the website will be inefficient.***

### The Solution
For *dynamically* or *regularly-changing* components, something like a JavaScript **variable** would be effective.

```html
<div id="weather-details">
	<h1>`${temperatureVariable} °C`</h1>
	<h4>New Delhi, India</h4>
</div>
```


>[!warning]
>This is not an actual working piece of code. It is just for illustrative purposes.

<br>

This is one of the many functions of **React**.
* It enables combining HTML with JavaScript
* Making components dynamic
* Adding logic to HTML elements directly
