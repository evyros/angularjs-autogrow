# angularjs-autogrow
AngularJS directive for auto-grow / auto-resize of textarea elements on typing.

 * Works in all cases: expands on line breaks and word breaks.
 * Great Performance: minimal DOM manipulation and no watchers.
 * Allows limitation of auto-growing so a scrollbar will appear after X lines of content.

## Installation via NPM
```npm install angularjs-autogrow --save```

######

## Usage:

Include `angular-autogrow.min.js` file in `<head>` section of the HTML:

```html
<script type="text/javascript" src="angularjs-autogrow.min.js"></script>
```

Include `angularjs-autogrow` dependency in your angular module:
```javascript
var app = angular.module("app", ["angularjs-autogrow"]);
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


### Autogrow on css properties change

You can define which CSS properties have to be watched in order to trigger the auto-growing:
```html
<textarea autogrow="font-family,font-size"></textarea>
```