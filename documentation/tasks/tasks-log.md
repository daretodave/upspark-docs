<!--TITLE:task.log()-->
<!--ABOUT:The log action will append the argument to the Upspark log.-->

The log method will append the argument to the [log](/tutorial#logs).

```javascript
task.message(message = '', error = false)
```
Helpful for debugging issues.

```javascript
export function task() {
	this.log(":-)");

	return "Look in the log";
}
``` 