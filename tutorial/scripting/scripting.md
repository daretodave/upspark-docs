<!--TITLE:Scripting-->
<!--ABOUT:Use the platform script to create and export commands.-->

Upspark will load any [exported](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export#Browser_compatibility) declarations from the **platform** script. Here's a hello task inside the **platform.js** file -

```javascript

export function hello() {
	return "Hello " + require('os').userInfo().username;
}

```