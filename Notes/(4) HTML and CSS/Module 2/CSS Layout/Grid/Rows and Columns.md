It involves a series of steps to follow.

### Defining Rows and Columns
In order to place children components according to the column and row numbers, **the columns and rows must first be defined**.

##### Properties
To define them, the CSS properties `grid-template-columns` and `grid-template-rows`  are used. 
```css
grid-template-columns: col col col col;
grid-template-rows: row row row;
```

| Code | What it means |
|--|--|
| `grid-template-columns` | Used to define columns in a grid |
| `col col col col` | The number of columns to create of width `col` |
| `grid-template-rows` | Used to define the rows of a grid |
| `row row row` | Creates 3 rows of width `row` |


##### Example
This would create 3 columns of width, $200px$, $100px$ and $200px$, and 2 rows of width, $300px$ and $150px$.

```css
grid-template-columns: 200px 100px 200px;
grid-template-rows: 300px 150px;
```
<br>

>[!info] `fr`
>It is another relative unit in CSS. It stands for `fraction`. So, `1fr` means *1 fraction*. 
>
>```css
>grid-template-columns: 1fr 1fr 1fr;
>```
>The above code says, *Create 3 columns with width 1 fraction or 1 part of the total width of the container.*
>![[Pasted image 20231104182733.png|250]]
>
>```css
>grid-template-rows: 3fr 1fr;
>```
>The above code would create 2 rows. The first row's width would be 3 parts and the second one's would be 1 part.  
>
>![[Pasted image 20231104182700.png|250]]

<br>

> [!tip]
> Say you have to create a grid with 10 columns. Rather than writing the code as 
> ```css
> grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr  1fr 1fr 1fr 1fr;
> ```
> The `repeat()` function should be used to make the code cleaner. The above code can be written as,
> ```css
> grid-template-columns: repeat(10, 1fr);
> ```
> It says, *Write `1fr` 10 times*.

<br>

### Placing components 
Next comes positioning the children with reference to the column and row numbers.

##### Properties
This is done using the properties `grid-column` and `grid-row`.
```css
grid-column: start-column / end-column;
grid-row: start-row / end-row;
```

| Code | What it means |
|--|--|
| `grid-column` | Used to define the position of a child with respect to column number |
| `start-column / end-column` | Place the child component from column number `start-column` to `end-column` |
| `grid-row` | Place the component according to the row number |
| `start-row / end-row` | Place the child from row number `row-start` to `row-end` |


##### Example
To place a child component like this,

![[Pasted image 20231104185206.png|350]]


```css
/* place the box from column line number 1 and cover the next 2 columns */ 
grid-column: 1 / span 2;

/* place the box from row line number 1 and cover the next 1 row */
grid-row: 1 / span 1;
```
<br>

>[!info]
> `span n` basically means *cover n columns/rows*.
> ```css
> grid-column: 2 / span 3;
> ```
> This means *start from column 2 and cover the next three columns*. This is the same as,
> ```css
> grid-column: 2 / 5;
> ```