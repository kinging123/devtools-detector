# detect-devtools
Detect whether DevTools is open, using `debugger;` statement

This project uses the code in [this dev.to article](https://dev.to/composite/a-simple-way-to-detect-devtools-2ag0)
by @composite.

It uses a similar API to the one created by @sindresorhus in 
[sindresorhus/devtools-detect](https://github.com/sindresorhus/devtools-detect), 
only it passes the `isOpen` property directly without the orientation.

```html
<script src="node_modules/devtools-detector/main.js"></script>
<script type="module">
	// Get notified when it's opened/closed or orientation changes
	window.addEventListener('devtoolschange', event => {
		console.log('Is DevTools open:', event.detail.isOpen);
	});
</script>
```