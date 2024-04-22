User data can be accepted in many forms and formats. 

### Text
For plain text such as *username*, *description* or fields alike.
```html
<input type="text">
```

### Password
It includes a toggle button to show or hide the password. It is hidden by default.
```html
<input type="password">
```

### File
To choose a file from the system memory.
```html
<input type="file">
```

### Time 
Data is input in the time format.
```html
<input type="time">
```

### Reset
A button to reset all the input fields to empty in a form.
```html
<input type="reset">
```

>[!note]
>Despite being an `<input>` tag, it is rendered as a button. 

<br>

### URL
For entering a URL with the correct format.
```html
<input type="url">
```

### Color
To select a color from a color picker.
```html
<input type="color">
```

### Range 
Renders a slider to select a value between an upper and lower limit.
```html
<input type="range" min="-100" max="100">
```

>[!tip]
>To display the current value of the slider, an `<output>` semantic element is used. Along with the `oninput` attribute which specifies *the function to execute when an input is given*.
>```html
><input type="range" min="-100" max="100" value="5" oninput="this.nextElementSibling.value = this.value">
><output>5<output>
>```
>This code basically says *If an input is given to the slider, change the value of the next element, i.e. the output element to the current value of the slider.*

<br>

### Radio
It can be used when to select only one value of some given options of the same property or `name`.
```html
<input type="radio" name="input-type" value="Text">
<input type="radio" name="input-type" value="Password">
<input type="radio" name="input-type" value="Number">
```

>[!tip]
>Radio buttons for the same property can be grouped using the `<fieldset>` HTML element. 
>```html
><fieldset id=input-type>
>	<input type="radio" value="Text">
>	<input type="radio" value="Password">
>	<input type="radio" value="Number">
></fieldset>
>```
>It serves the same functionality as the `name` attribute.

<br>

### Checkbox
Same functionality as radio, the difference being that it allows for multiple values to be chosen for the same property or `name`.
```html
<input type="checkbox" name="input-type" value="Text">
<input type="checkbox" name="input-type" value="Password">
<input type="checkbox" name="input-type" value="Number">
```

