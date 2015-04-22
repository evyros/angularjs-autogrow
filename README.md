# Angular-Autogrow
Angular directive for auto-grow / auto-resize of textarea elements on typing.

 * Works in all cases: expands on line breaks and word breaks.
 * Great Performance: minimal DOM manipulation and no watchers.
 * Allows limitation of auto-growing so a scrollbar will appear after X lines of content.

A full explanation of the code can be found on my [blog post](http://codingaspect.com/blog/textarea-auto-grow-resizing-textarea-to-fit-text-height) along with a jQuery plugin and an Angular directive with this technique.

#### Install via Bower
```bash
bower install angular-autogrow
```

######

## Usage:

Include `angular-autogrow.min.js` file in `<head>` section of the HTML:

```html
<script type="text/javascript" src="angular-autogrow.min.js"></script>
```

Include `angular-autogrow` dependency on your angular module:
```javascript
var app = angular.module("app", ["angular-autogrow"]);
```

It's also recommended to add those two CSS properties to make things stable:
```css
textarea {
	resize: none;
	box-sizing: content-box;
}
```

Add the directive to the textarea element:
```html
<textarea autogrow></textarea>
```

######


## More Options:

### Limit Autogrow Lines

You can limit the auto-growing of the textarea element by using `max-lines` attribute:
```html
<textarea autogrow max-lines="3"></textarea>
```


### Set Initial Rows

You can set the initial line number using `rows` attribute:
```html
<textarea autogrow rows="1"></textarea>
```