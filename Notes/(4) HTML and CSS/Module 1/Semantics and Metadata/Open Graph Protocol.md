Established by Meta, it basically creates a preview of a webpage, when shared, in terms of its metadata.

For instance, the ads posted on social media platforms like *Facebook* and *YouTube* have
* An Image for preview
* The URL of the webpage
* A brief description 
![[Pasted image 20231029160845.png|400]]

This is made possible due to the Open Graph Protocol.

### Usage
It, also, involves meta tags but with the the prefix `og` to depict `Open-Graph`. The five basic meta tags that **must** be in a webpage are understated.

| `property` | `content` |
|--|--|
| `og:title` | The title of the webpage |
| `og:description` | A brief of what the webpage contains |
| `og:image` | A hyperlink to the image to be shown in preview |
| `og:url` | URL of the webpage |
| `og:type` | The type of webpage <br> ![[Pasted image 20231029162639.png\|70]] |

>[!note]
>These are the values of the `property` attribute of the `<meta>` tag. The `content` attribute should contain the actual values.

### Example
An example for the [[Metadata#Example|website]] would be
```html
<!DOCTYPE html> 
<html>
	<head>
		<meta property="og:title" content="Front-End Development Basics"> 
		<meta property="og:description" content="Describing the concepts of Front-End Development"> 
		<meta property="og:url" content="https://www.frontenddev.com/basics">
		<meta property="og:image" content="./images/logo.png">
		<meta property="og:type" content="website"> 
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