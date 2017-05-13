<!--TITLE:Background-->
<!--ABOUT:Use the background action to postpone the resolution of a task -->

It's possible to postpone or delay a task's completion. This is done by using a task function witch is bound to the **this** object for commands. 

```javascript
export function delay() {
	this.background(); // Task function

	setTimeout(() => this.message('Chugging along'), 1000); //After one section, "Chugging along" is rendered

	setTimeout(() => this.complete('All done'), 2000); //After two seconds, "All done" is displayed 

	this.message('Starting...'); //This message is rendered right away, before the other two
}
```

Note, because background, message and complete depend on the this object; the command declaration can not use fat arrow syntax.
 
Learn more about task functionality in the [documentation](/documentation#tasks).

