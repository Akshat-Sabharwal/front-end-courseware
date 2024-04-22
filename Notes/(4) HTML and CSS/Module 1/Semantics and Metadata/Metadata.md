*meta* means *about or self-reference*. **Metadata**, thus, translates to ***data about data***. 
It basically is a summary of data.
### SEO
Say, on searching "*Front End Development*" on Google, certain results concerning Frontend Dev. appear. But how does the browser know what "*Front End Development*" means and come up with likewise results?

![[Pasted image 20231029143424.png|300]]
Search-Engine Optimization, or SEO for short, is a technique used by browsers to filter searches according to the ***Metadata** of a webpage*. 

In the example above, the webpages that appear in the search results have the metadata of *Front-End Development*. 

### Meta Tags
To make the webpage appear in a certain search result, its metadata must be added.
The open HTML tag, `<meta>` is used in this case. It has two main attributes.

| Attribute | Usage |
|--|--|
| `name` | The parameter whose metadata is to be specified |
| `content` | Value of the parameter |

* #### `name`
The attribute `name`, commonly, has the following values.

| Value | What it means |
|--|--|
| `author` | It tells who the author  of the webpage is |
| `language` | The language the webpage is in |
| `description` | A summary or brief of the content of the webpage |
| `robots` | Tells the Search Engine how to analyze the webpage |
| `rating` | For which age group is the webpage suited |

* #### `content`
It is the actual data or *value* of the `name` parameter.

| `name` | `content` |
|--|--|
| `author` | John Doe |
| `language` | English |
| `description` | This webpage describes what Metadata is |
| `robots` | `index` → *read the page* <br> `noindex` → *don't read the page* <br> `follow` → *visit all the links in the page, as well* <br> `nofollow` → *don't visit the links in the page* |
| `rating` | Suitable for all |


### Example
A webpage to show up in the search result *Front-End Development* would be
```html
<!DOCTYPE html>
<html>
	<head>
		<meta name="author" content="John Doe">
		<meta name="description" content="Describing the concepts of Front-End Development">
	</head>
	
	<body>
		<header>
			<img src="logo.png">
			<h1> Heading </h1>
		</header>
		
		<main>
			<section>
				<h3>What is it?</h3>
				<p>Lorem Ipsum Dolor Sit Amet...</p>
			</section>
		</main>
		
		<footer>
			<h3> Contact Us </h3>
			<menu>
				<li>Youtube</li>
				<li>Facebook</li>
				<li>Instagram</li>
			</menu>
		</footer>
		
	</body>
</html>
```