<!--TITLE:API-->
<!--ABOUT:Upspark comes pre-packaged with a light weight promised based API to help with simple tasks.-->

Upspark comes prepacked with a light weight promise based API to help with simple tasks.

| Route | Description |
|-------|-------------|
| [upspark/safe](/documentation#safe) |  Get values stored in the [safe](/tutorial#safe). |
| [upspark/platform](/documentation#platform) |  Get platform commands or reload the platform script. |
| [upspark/runner](/documentation#runner) | Control the main runner and execute tasks.  |
| [upspark/settings](/documentation#settings) | Get and set [settings](/tutorial#settings).  |
| [upspark/desktop](/documentation#desktop) | Open host applications and control the clipboard.  |
| [upspark/file](/documentation#file) | Basic file operations e.g. stat, copy, move, delete, create and more.  |
| [upspark/net](/documentation#net) | Make HTTP calls with the request api.  |

Here's an example of using the API in **platform.js**

```javascript
import Desktop from 'upspark/desktop'

// Attach the argument to the clipboard and return the previous result
export const replace = (arg) => Desktop
	.getClipboardText()
	.then(text => {
		Desktop.setClipboardText(arg);
		
		return text;
	})
```

Learn all the API functionality in the [documentation](/documentation).