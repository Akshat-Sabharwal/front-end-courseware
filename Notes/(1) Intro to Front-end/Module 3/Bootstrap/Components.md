### Grid System
A way of *containerizing* or structuring elements within a document provided by Bootstrap. There are 3 main constituents of a **grid system**.

![[Pasted image 20230914165032.png]]

* ##### Container
  It is the *box* which encompasses all the elements within.
  <br><br>
* ##### Row
  It is, as the name conveys, a *row* or a horizontal sub-box with a percent width of the **container** with the length of the **container**.
  <br>
  
  | Prefix | Description | Instance |
|--|--|--|
| `-cols-{breakpoint}-#` | Size of each column in the row | `.row-cols-sm-3` |
<br>

* ##### Column
  It is just a **row** but vertical.

  | Prefix | Description | Instance |
|--|--|--|
| `-sm, -md, -lg, -xl, -xxl` | Breakpoints for `min-width` of device | `.col-*` |
| `-1, -2, -3, -4, -6, -12` | Width of the column | `.col-{breakpoint}-*` |
<br>

### Card
A flashcard-like structure useful for product catalogue, features and cases alike.

![[Pasted image 20231125164603.png]]



```html
<!DOCTYPE html>

<html lang="en">
<head>
	<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css">
</head>
<body>
    <div class="container">
        <div class="row">
            <div class="col">
	            <div class="card"></div>
            </div>
            <div class="col">
	            <div class="card"></div>
            </div>
        </div>

        <div class="row">
            <div class="col">
	            <div class="card"></div>
            </div>
        </div>
    </div>

    <script src="../Bootstrap/bootstrap-4.3.1-dist/js/bootstrap.min.js"></script>

</body>
</html>
```

>[!note]
>The height of the card is variable, i.e. it depends on the *amount* of content that is in the card.


