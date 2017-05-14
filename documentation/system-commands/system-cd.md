<!--TITLE:cd-->
<!--ABOUT:The cd task will set Upspark's current working directory.-->

```javascript
:cd null|...path
```

The cd task will set Upspark's current working directory to the targeted path. By default this the [platform directory](/tutorial#install).

This task can accept the targeted path in chunks.
```javascript
:cd ./ folderParent folderChild folderX
```

Which is equivalent to
```javascript
:cd ./folderParent/folderChild/folderX
```

To reset the current working directory to the default location, pass no arguments to cd
```javascript
:cd
```