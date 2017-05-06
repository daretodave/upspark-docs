<!--TITLE:REPL-->
<!--ABOUT:Use the history view of Upspark to communicate with a REPL process.-->

You can send messages to a long running process by entering REPL mode.

This is done by focusing on the command in historical view -
![Focus on REPL](./image/repl-start.png)

Then by pressing the **right arrow**. This will cause Upspark to toggle REPL mode, in which any command will be proxied to the focused task. 

In this case, to the node.js process.
![REPL mode](./image/repl.png)

History from the current REPL session will display in the command output.
![REPL mode](./image/repl-example.png)

Press **left arrow** to exit REPL mode.