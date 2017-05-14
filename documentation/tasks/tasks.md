<!--TITLE:Tasks-->
<!--ABOUT:Upspark provides binds a few methods to the this object when executing -->

There are a few methods bound to the **this** object when executing tasks.

Because of the nature of the **this** object, these methods can not be used within a fat arrow declaration of a task.

This will work

```javascript
export function background() {
	this.background();

	setTimeout(() => this.complete('Done'), 1000); // Fat arrow is okay in this case because the this scope is 
							// in the outer closure
}
``` 

This will not work (*this is not defined*)

```javascript
export const background = () => {
	this.background();

	setTimeout(() => this.complete('Done'), 1000);
}
```

Of-course, this drawback is only a drawback if your using these task functions! 