<!--TITLE:Commands-->
<!--ABOUT:Upspark commands are executed by typing the command name and pressing enter.-->

To run a task, type the command and press *enter*. The format of a command is -
```
[type]task[arg1 arg2 arg3 argN...]
```
The command type decides how Upspark will execute the task. When no type is provided, Upspark will execute the task against your platform script *(labeled Platform below)*.

| Type      | Prefix   | Execution | Example |
|-----------|-------|-----------|---------|
| Platform  | **#** | Upspark will attempt to execute any exported function in *platform.js* that has the same name as the **task**. Any arguments are passed as arguments to the function. If possible, The runner will display the returned result. *[see scripting further down](/tutorial#scripting)* | hello  |
| System  | **:** | Upspark will run the task against available system commands. Note, system commands are not user controlled. *[see a full list of system commands here](/documentation#system-commands)* | :reload :clear :platform :settings
| Runtime | **>** | Upspark will proxy the task and the arguments against the current machine's shell. | >ping >node >ls-a


Pressing **ESCAPE** will clear the current command input.
