<!--TITLE:runner.css-->
<!--ABOUT:Upspark will optionally load a runner.css file if this exists. Use this to theme the runner.-->

When **runner.css** exists in the platform directory, Upspark will apply this CSS file to the runner's look and feel.

Note, **[:reload theme](/documentation#system-reload)** will reload this file.

Here's an example of the illuminated theme (white background). 

```css
#runner {
    background: rgba(255, 255, 255, 0.8);
}

#runner.runner-repl {
    animation: pulse 5s infinite;
}

@keyframes pulse {
    0% {
        background: rgba(255, 255, 255, 0.8);
    }
    50% {
        background: rgba(140, 140, 140, 0.7);
    }
    100% {
        background: rgba(255, 255, 255, 0.8);
    }
}

.command__title {
    color: rgba(0, 0, 0, 0.67);
}
#runner-path {
    color: black;
}
#runner-input {
    color: black;
}
#runner-debug {
    color: black;
}
.up-title {
    color: black;
}
.runner__output {
    color: black;
}
.runner__output {
    color: black;
}
.command__response {
    color: black;
}
up-command-argument {
    color: black;
}

.key.selected {
    color: black;
}
.key.selected:hover {
    color: black;
}
.key:hover:not(.selected) {
    color: black;
}
```