Just like Parent and Child classes in JavaScript, Components are named on the basis of hierarchy.

### Example
Say there are two components named `Article` and `Main`. 
```jsx
export default function Article() {
	return (
		<>
			<h1>Heading</h1>
			<p>Lorem ipsum dolor sit amet...</p>
		</>
	);
}
```

```jsx
export default function Main() {
	<Article />
}
```

Here, `Article` is considered a ***Child*** of `Main` and `Main` is the ***Parent*** of `Child`.