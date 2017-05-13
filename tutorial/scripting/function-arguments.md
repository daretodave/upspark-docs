<!--TITLE:Parameters -->
<!--ABOUT:Pipe arguments from the runner to the platform with function parameters.-->

Here's an example of a basic command that simply returns the argument to the user.

````javascript
export function echo(argument) {
	return 'You said "' + argument + '"';
}
````

The task title is **echo**. To execute the command, type **echo** with the argument on the runner.

![Echo Command](.\image\echo.png)

Because **argument** is used without any existence checking, when no argument is supplied -

![Echo Command, with no argument](./image/echo-argless.png)
