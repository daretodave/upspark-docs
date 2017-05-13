<!--TITLE:Importing-->
<!--ABOUT:Upspark can be expanded with local modules or NPM modules.-->

You can leverage script imports to help separate code logic or include a NPM module.

Consider the following platform directory structure
```
.upspark/
-----> platform.js
-----> lib/
--------------> logger.js
```

Here's logger.js
```javascript
export const log = (message) => message.slice(0, 140);

```

Here's platform.js using the log function and renaming it to debug 
```javascript
import {log} from './lib/logger';

export {log as debug};
```

Now the command **debug** will return the first 140 characters of the argument.
