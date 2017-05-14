<!--TITLE:task.progress()-->
<!--ABOUT:The progress task will update the user with the current state of the task.-->

You can use the progress task to change the intermediate task progress bar to an actual progress bar with the provided progress.

```javascript
task.progress(progress = -1, message = null)
```

Additionally, the message will append to the history section instead of the task output. This is helpful for debugging.

```javascript
export function task() {
	this.background();

	setTimeout(() => this.progress(5), 100);
	setTimeout(() => this.progress(10, "Working Hard!"), 200);
	setTimeout(() => this.progress(60), 300);
	setTimeout(() => this.progress(80, "Almost there!"), 400);

	setTimeout(() => this.complete(), 500);
}
``` 