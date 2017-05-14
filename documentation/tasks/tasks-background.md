<!--TITLE:task.background()-->
<!--ABOUT:The background action will let Upspark know that your task can not resolve yet.-->

The background method will flag your task execution as manually resolved. 

```javascript
task.background(isBackgroundTask = true)
```

Your return value will be ignored and the only way to finish the task is by using [complete](/documentation#tasks-complete), [abort](/documentation#tasks-abort) or [error](/documentation#tasks-error).

```javascript
export function task() {
	this.background();

	setTimeout(() => this.complete('Done'), 1000);

	return "HELLO"; // ignored
}
``` 