The style of text wrapped by elements around can be modified using some basic declarations.

### Font Size and  Family
The `font-size` property accepts units such as `px`, `em` along others and the `font-family` demands for the font-style followed by the family to which it belongs.

```CSS
p {
	font-size: 20px;
	font-family: "Roboto", sans-serif;
}
```

### Text Decoration
Text can be *decorated* or stylized by underlining or striking the text.

```CSS
p {
	text-decoration: underline red dash 3px;
}
```

| Value | Usage |
|--|--|
| `underline` | Type of decoration |
| `red` | Color of the decoration (underline here) |
| `dash` | Stroke of the decoration (----- here) |
| `3px` | Width of the decoration |


# Color
Color of font and other elements can be customized in CSS using multifarious color models.

### RGBA
Standing for **Red-Green-Blue-Alpha**, RGBA is a very popular color model. Each one of RGBA is a parameter which tells how much of that color is mixed to get a composite color.

```CSS
p {
	color: rgba(255, 255, 255, 1);
}
```

| Parameter | Usage | Range |
|--|--|--|
| RGB | Saturation of RGB in the color | [0-255] |
| Alpha | Transparency of the mixed color | [0-1] |

### HSL
Standing for **Hue-Saturation-Lightness**, HSL is yet another color model which CSS supports.

```CSS
p {
	color: hsl(120, 100%, 50%);
}
```

| Parameter | What it means | Range |
|--|--|--|
| Hue | The color | [0°-360°] |
| Saturation | How much of the color is in there | [0-100%] |
| Lightness | How light the color is | [0-100%] |

![[Pasted image 20230909161044.png|400]]