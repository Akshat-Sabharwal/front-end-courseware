HTML allows for adding videos in a webpage. 

### Tag
This can be done using the `<video>` tag. It has the following attributes.

| Attribute | Usage | Example |
|--|--|--|
| `width`, `height` | Define the dimensions of the video player | `<video height="300px" width="500px">` |
| `controls` | Add controls like pause and fast-forward to the player | `<video controls>` |

It is paired with the open tag, `<source>`, which specifies from where the video file is added or its *source*.

| Attribute | Usage | Example |
|--|--|--|
| `src` | Defines the actual source or location of the video file | `<source src="videos/personal/dance.mp4">` |
| `type` | Specifies the format of video used | `<source type="video/mp4">` <br> `<source type="video/webm">` <br> `<source type="video/ogg">` |


### Example
This will add a video player with controls of dimensions 300x500 playing the video `dance` in `ogg` format.
```html
<video height="300px" width="500px" controls>
	<source src="dance.ogg" type="video/ogg">
</video>
```
