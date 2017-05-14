<!--TITLE:task.message()-->
<!--ABOUT:The message action will append the argument to the task result.-->

The message method will append the argument to the task result.

```javascript
task.message(type = 'out' || 'error', message = '')
```

```javascript
task.message(message = '')
```

This is helpful for streaming results.

```javascript
export function task() {
	this.background();

	setTimeout(() => this.message('A'), 500);
	setTimeout(() => this.message('B'), 1000);
	setTimeout(() => this.message('error', 'C'), 1500); 

	setTimeout(() => this.complete(), 2000);
}
``` 