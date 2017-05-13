<!--TITLE:Null Parameters-->
<!--ABOUT:Here are some tips on resolving null parameters from the runner.-->

Here's an updated echo command with null checking -

````javascript
export function echo(argument) {
	if(!argument) {
		argument = 'nothing';
	}

	return 'You said "' + argument + '"';
}
````

Alternatively, you can use simply use default arguments -
```javascript
export function echo(argument = 'nothing') {
	return 'You said "' + argument + '"'; 
}
```

Since Upspark supports ECMAScript 7, here's the same task with an arrow function expression and template literals.
```javascript
export const echo = (argument = 'nothing') => `You said "${argument}"`;
```
