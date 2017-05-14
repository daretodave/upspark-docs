<!--TITLE:env-->
<!--ABOUT:The env task can be used to manage Upspark's environment variables sent to commands.-->

```javascript
:env null|SET VAR VALUE|DELETE VAR
```

The env task helps establishing temporary environment variables used by tasks. When in a child process (platform command context), values displayed in env can be accessed in the [process.env](https://nodejs.org/api/process.html#process_process_env) property.

Set a property (*a=xxx*)
```javascript
:env set a xxxx
```

Remove a property (*a*)
```javascript
:env delete a
```
 
List properties
```javascript
:env
```