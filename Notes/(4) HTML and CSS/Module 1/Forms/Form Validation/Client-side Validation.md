For efficient verification of results, the data validation process is divided in two parts. The first one being **Client-Side Validation**. Some of the techniques used for the same are understated.

### Input-type Comparison
The attribute `type` of the `<input>` tag is compared with the type of actual input. If it is correct, the process proceeds, else an alert message is prompted.

### Significance
Another one is to check if data is entered in all the ***required*** fields or not. If not, an alert is shown.
>[!info]
>A required field is the one that needs to be filled else the form won't be submitted. 
>This can be done using the `required` attribute.
>
>```html
><input type="text" required>
>```

### Specifying Range
Using `minlength` and `maxlength` to set limits to word count in text-type or number-type input field is another option. 