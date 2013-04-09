# Time polyfill (aka Timepikr)

## Use
```html
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">
	<!-- ... -->
	<link rel="stylesheet" href="timepicker.css">
	<!-- ... -->
</head>
<body>
	<!-- ... -->
	<input type="time" id="timepikr-me">
	<!-- ... -->
	<script src="timepicker.js"></script>
	<script>
		var picker = new TimePikr({
			element: document.getElementById('timepikr-me');
		});
	</script>
</body>
</html>
```

### Extra! Conditional loading

```javascript
Modernizr.load({
	test: Modernizr.inputtypes.time,
	nope: ['timepicker.css', 'timepicker.js'],
	callback: function() {
		var picker = new TimePikr({
			element: document.getElementById('timepikr-me');
		});
	}
})
```

## Author

[Emilio Cobos Álvarez](http://emiliocobos.net)

## Todo

* Add keyboard support