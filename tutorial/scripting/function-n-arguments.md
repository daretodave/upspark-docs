<!--TITLE:Many Parameters-->
<!--ABOUT:Upspark will bind all the arguments from the runner to the task function.-->

Upspark will still call the task's function with the runner arguments even when the parameters are not provided in the method signature.

This means you can use the **rest** parameter syntax to catch a variable number of arguments -
```
export function roots(...args) {
	return Array.from(args).map(Math.sqrt);
}
```

Alternatively use the **arguments** object. This will only work for traditional function expressions.
```
export function roots() {
	return Array.from(arguments).map(Math.sqrt);
}
```