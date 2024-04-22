Assume that you have to create 3 components each with a different heading element. So, the only difference is in the children property of the VDOM.

![[Pasted image 20231124144211.png|300]]

Creating 3 different components which have the same structure would not be the most efficient  way. 

### Component Composition
It basically means *the structure of components or what they contain*. It has two main features depending upon the children of the components.  
<br>

* ##### Containment
Often, the components do not know their children, beforehand. So, instead of creating the complete component, its children are included in the *props* to be passed to it.

  For instance, a `Card` component that is re-used but with different children elements can be created as follows.
  ```jsx
function Card({ children }) {
	<div className="card">
		{ children }
	</div>
}
  ```

  At the time of rendering the component, the children can be specified just as in regular HTML.
  ```jsx
function App() {
	<Card>
		<h1>This is an h1 heading</h1>
		<p>Lorem ipsum dolor sit amet</p>
	</Card>

	<Card>
		<img src="./assets/images/someimage.png" alt="Some Image" />
		<p>Lorem ipsum dolor sit amet</p>
	</Card>
}
  ```

<br>

* ##### Specialization
When a component created using the Containment pattern, *i.e.* *creating a component and mentioning its children later on*, it can be used just like a [[Abstraction|base class]] while using Abstraction to create the **extended classes** or components, here.

For instance, the `Card` component created above can either have a `<img>` element or an `<h1>` element. In such a case, 2 components can be built on top of the `Card` component.

```jsx
function Card({ children }) {
	<div className="card">
		{ children }
	</div>
}

function ImageCard({ imageSource }) {
	return(
		<Card>
			<img src={imageSource} />
			<p>Lorem ipsum dolor sit amet</p>
		</Card>
	);
}

function HeadingCard({ headingText }) {
	return(
		<Card>
			<h1>{headingText}</h1>
			<p>Lorem ipsum dolor sit amet</p>
		</Card>
	);
}
```
