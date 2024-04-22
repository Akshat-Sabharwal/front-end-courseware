Just like videos, audio can be added in a webpage using HTML. 

### Tag
This can be done using the `<audio>` tag with the following attributes.

| Attribute | Usage | Example |
|--|--|--|
| `controls` | Add controls like pause and fast-forward to the player | `<audio controls>` |

It is also used along with the `<source>` tag which serves the same purpose of mentioning the location of the file.

| Attribute | Usage | Example |
|--|--|--|
| `src` | Defines the actual source or location of the audio file | `<source src="videos/personal/dance.mp3">` |
| `type` | Specifies the format of audio used | `<source type="audio/mpeg">` <br> `<source type="audio/wav">` <br> `<source type="audio/ogg">` |


### Example
This will add an audio player with controls playing the audio `music` in `mp3` format.
```html
<video controls>
	<source src="dance.mp3" type="audio/mpeg">
</video>
```

>[!note]
>`mp3` stands for `MPEG Audio Layer 3`. Thus, `mpeg` is used for `mp3`. 
>Also, `MPEG` stands for *Media Players Experts Group*.
 
