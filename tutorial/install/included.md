<!--TITLE:Included-->
<!--ABOUT:Upspark requires a few important files that get created on first launch.-->

After launching Upspark, a few important files will be created.

If these core files are deleted, Upspark will create a new one in it's place with the default contents. The only exception is when the package.json is modified to load an alternative main script; Upspark will not create platform.js

| File          | Purpose                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| package.json  | Can be used to install packages with npm or yarn. Additionally the main flag in this document can be changed to point to a new platform script. |
| settings.json | Stores the settings for Upspark. Includes configuration such as location, size, theme and hotkey.                                               |
| upspark.log   | Can be used to further understand bugs and issues when using the runner.                                                                        |
| platform.js   | The default entry point for Upspark. This can be changed in settings.json.                                                                      |
