<!--TITLE:Scripting-->
<!--ABOUT:Use the platform script to create and export commands.-->

Upspark will load any [exported](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export#Browser_compatibility) declarations from the **platform** script. Here's a hello task inside the **platform.js** file -

```javascript

export function hello() {
	return "Hello " + require('os').userInfo().username;
}

```

Note, the command declaration does not have to be a function. Additionally the command does not have to have a return value.

The below declaration will still have the same effect. 

```javascript
export const hello = "Hello " + require('os').userInfo().username;
```

The important difference when using a variable vs. a function is that the variable will not be able to accept the arguments from the runner to perform logic.

Upspark will resolve a promise if the function returns one.

Here's a simulated 1000ms long wait on the hello function.
```javascript
export function hello() {
	return new Promise((resolve, reject) => { 
		setTimeout(() => resolve("Hello " + require('os').userInfo().username), 1000);	
	});
}
```

When no return value is provided, Upspark will simply finish the task with no output.

This may not be the desired effect. If instead your goal was to execute logic in the background and resolve the value later, you can either use the promise pattern **or** use [background](/tutorial#background-tasks) tasks.