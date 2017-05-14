<!--TITLE:task.complete()-->
<!--ABOUT:The complete method will resolve and end the task.-->

The complete action will end a task and append the argument to the task output. (*a message and abort action*)  

```javascript
task.complete(message = '')
```

```javascript
export function task() {
	this.background();

	setTimeout(() => this.complete('Done'), 1000);
}
``` 