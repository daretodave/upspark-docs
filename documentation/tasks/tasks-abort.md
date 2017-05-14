<!--TITLE:task.abort()-->
<!--ABOUT:The abort action will end the child process holding the current task.-->

The abort method will end the current task, no questions asked.

```javascript
task.abort(message = '', isNotError = false)
```

Because each task is it's own child process there's no fear of background actions still being executed.

```javascript
export function task() {
	this.background();

	setTimeout(() => this.abort()), 500);

	setTimeout(() => this.complete('Done'), 1000); // Never executed
	
}
``` 

By default, it will throw a fatal error. Flag isNotError as true to indicate this was not an error.