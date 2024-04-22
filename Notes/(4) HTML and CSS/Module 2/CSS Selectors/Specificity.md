Just a fancy word meaning giving importance to certain objects on the basis of superiority.

CSS uses specificity in selectors. It is, thus, called **Selector Specificity**.

### How?
CSS has a hierarchy of selectors. This means that some selectors are more *powerful* than others.

![[Pasted image 20231104225727.png|350]]
##### Example
A CSS rule written using an element selector will be overridden by the one written in the inline style.

```css
/* styles.css */
p {
	color: blue;
}
```

```html
<!-- index.html -->
<p style="color: white;">
```

Herein, the font-color of the `<p>` element will be `white` and not `blue` ***because the Inline style has a higher specificity than the Element selector**.* 


### Why?
When working with larger codebase, it is natural and often to have **rule conflicts**. Selector Specificity solves the issue of errors and unwanted design and layout.

Developers, therefore, use more ID selectors than other selectors because of its higher specificity.

>[!info]
>**Rule conflicts** are when multiple CSS rules are meant for the same property of the same element. 
>
