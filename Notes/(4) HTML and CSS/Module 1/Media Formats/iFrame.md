Not an Apple product rather an HTML element that allows to run a website inside another webpage.

![[Pasted image 20231030142326.png|300]]

It is used to run ads and mention social media posts in webpages and much more. But is considered insecure as the website to embed might be malicious.

### Tags
To add an iFrame, the `<iframe>` tag is used which has the following attributes.

| Attribute | Usage | Example |
|--|--|--|
| `src` | The URL of the website to embed | `<iframe src="https://www.google.com/search"></iframe>` |
| `height`, `width` | Set the dimensions of the iFrame | `<iframe height="240" width="320"></iframe>` |
| `allow` | To make the iFrame safe, certain restrictions can be imposed on it | `<iframe allow="geolocation 'none'; camera 'none'">` |

### Security
iFrames can be made more secure by using the attributes `allow` and `sandbox` to restrict certain permissions.

* #### `allow`
It is used to enable or disable permissions to the website embedded.
```html
<!-- To allow permissions -->
<iframe allow="camera; microphone; geolocation;"></iframe>

<!-- To disable permissions to the iframe -->
<iframe allow="camera 'none'; microphone 'none';"></iframe>
```

* #### `sandbox`
To impose even more restrictions such as the permission for not using JavaScript files or downloading files.
```html
<!-- To apply all restrictions -->
<iframe sandbox=""></iframe>

<!-- To allow certain permissions to the iframe -->
<iframe sandbox="allow-downloads allow-popups"></iframe>
```