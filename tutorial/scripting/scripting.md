<!--TITLE:Scripting-->
<!--ABOUT:Use the platform script to create and export commands.-->

Using the platform with your own script logic is as easy as exporting functions from the **platform.js** file.

## Reloading

When saving a command in platform.js, there's a couple of ways to reload commands.
- Restarting Upspark
- Clicking **Reload** in the task bar context menu

The simplest way to reload commands is by executing **:reload** in the runner -

![Reload Command](./image/reload.png)

## Command Logic

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

## Null Checking
----------

Here's an updated echo command with null checking -

````javascript
export function echo(argument) {
	if(typeof argument === 'undefined') {
		argument = 'nothing';
	}

	return 'You said "' + argument + '"';
}
````

```javascript
export const echo = argument => `You said "${}"`;
```
       

Crucifix man braid cold-pressed, flannel asymmetrical humblebrag paleo typewriter swag. Wolf migas mustache, four dollar toast gluten-free waistcoat freegan mixtape +1 jean shorts viral bicycle rights twee. Narwhal tumeric stumptown swag banjo waistcoat sartorial listicle. Mumblecore 8-bit small batch wolf wayfarers fam. Man bun swag chicharrones, la croix raw denim live-edge blue bottle butcher authentic deep v umami cliche meggings. Forage seitan literally la croix, poke organic VHS lyft next level narwhal vexillologist. Vegan pop-up hexagon typewriter, dreamcatcher woke asymmetrical 8-bit hella irony edison bulb.

Helvetica meggings hexagon lo-fi, mumblecore deep v mixtape etsy. Sriracha slow-carb tbh pitchfork pok pok. Bespoke cold-pressed dreamcatcher jean shorts affogato. Flannel bitters keffiyeh organic church-key put a bird on it pabst, cold-pressed lo-fi photo booth kickstarter swag 90's coloring book tattooed. Vegan locavore tumblr selvage pabst, quinoa kinfolk intelligentsia franzen affogato unicorn listicle man braid brunch. Church-key selfies literally hexagon flannel franzen, hell of pug XOXO. Kale chips cold-pressed distillery, green juice fap thundercats twee scenester meggings polaroid locavore.
