<!--TITLE:open-->
<!--ABOUT:The open task will open the argument with the default file association.-->

```javascript
:open null|...path
```

The open task will open the target with the default file association. 
- Folders will open with the default file explorer

If the path argument provided is not absolute, it will be pre-pended with Upspark's current working directory (*platform directory by default*)