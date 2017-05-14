<!--TITLE:task.error()-->
<!--ABOUT:The error action will end the current task and display the argument as an error.-->

Just like the [complete](/documentation#tasks-complete) action, the abort action will end a task and append the argument to the task output as an error. (*an abort*)  


```javascript
task.error(message = '')
```

```javascript
export function task() {
	this.background();

	setTimeout(() => this.error('Not done'), 1000);
}
``` 