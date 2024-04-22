Bootstrap associates UI elements with pre-defined `class` names for `<div>`  containers.

### How to use it?
Class names usually have a format of `{Base-Class}-{Contextual-Class}`

* Base-Class → The basic Bootstrap component to be added
* Contextual-Class → The modification to be applied to the component 

```html
<html>
	<head>
		<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css">
	</head>
	<body>
		<div class="container">
			<div class="row">
				<div class="alert alert-primary">Message</div>
			</div>
		</div>
	</body>
</html>
```

Here, the `container` has been used to create a grid and `row`, to place the alert message in the first row of the grid.

### Some Common Bootstrap Components

| Bootstrap Component    | Bootstrap Classes                           | Description                                |
|------------------------|---------------------------------------------|--------------------------------------------|
| Grid System            | `container`, `container-fluid`, `row`, `col-*` | Used for creating responsive layouts based on a 12-column grid system. |
| Typography             | `text-*`, `font-weight-*`                  | Provides text styling options for headings, paragraphs, and alignment. |
| Buttons                | `btn`, `btn-primary`, `btn-secondary`, ... | Creates interactive buttons with various styles. |
| Forms                  | `form-group`, `form-control`, `input-group`, ... | Styles form elements like inputs, checkboxes, and select boxes. |
| Navigation             | `navbar`, `nav`, `nav-item`, `nav-link`, `dropdown`, ... | Helps create responsive navigation menus and bars. |
| Alerts                 | `alert`, `alert-*`                         | Displays alert messages and notifications. |
| Badges                 | `badge`, `badge-*`                         | Creates badges or labels for highlighting content. |
| Cards                  | `card`, `card-header`, `card-body`, ...    | Structured containers for content presentation. |
| Modals                 | `modal`, `modal-dialog`, `modal-content`, ... | Displays modal dialogs for additional content or forms. |
| Carousel               | `carousel`                                 | Creates image sliders or galleries.       |
| Utilities               | Margin and padding classes, text alignment, ... | Provides utility classes for spacing and alignment. |
| Responsive Classes     | `d-*-none`, `d-*-block`, `d-*-inline`, `d-*-flex`, ... | Controls element visibility and behavior on different screen sizes. |


