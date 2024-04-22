To define the changes made at each step, the **At-rule** `@keyframes` is used.

>[!info]
>An **at-rule** is a specific statement which tells the browser, when to behave according to the properties inside it.

Herein, the animation is first defined step-wise. It can, then, be used for multiple components by assigning them the animation.
### Syntax
```css
@keyframes animation-name {
	0% {
		/* CSS rule here */
	}
	50% {
		/* CSS rule here */
	}
	100% {
		/* CSS rule here */
	}
}

.component {
	animation: animation-name duration;
}
```

| Code | What it means |
|--|--|
| `@keyframes` | The **at-rule** to indicate the animation |
| `animation-name` | Name of the animation |
| `0% {}`, `50% {}`, `100% {}` | ***Keyframes*** or *steps* of the animation |
| `animation` | Property assigned to the component that needs to be animated |
| `duration` | The duration of the animation |


>[!note]
>Keyframes are percentage values. The above code will define what the components must look like when,
>* `0%` → when animation starts
>* `50%` → when animation is halfway-through
>* `100%` → when animation ends
>
>Also, the keyframes can have any percentage value.
>



### Example
This will create an animation of a square ***morphing*** or *changing its shape* into that of a circle.

```css
@keyframes sq-to-crc {
	0% {
		border-radius: 0;
	}
	
	100% {
		border-radius: 50%;
	}
}

.square {
	animation: sq-to-crc 2s;
}
```