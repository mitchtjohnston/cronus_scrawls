# Cronus Scrawls

## About
This is a simple repo to store all the various scripts for the Cronus Zen (and possibly Max if they are backwards compatible) created by myself and others that I have found useful or use on a regular basis.

## Cronus Zen Scripting
The language and file type used by the Cronus Zen (and Max) is based on C and is saved as .gpc files. While using a visual text editor like VSC for syntax is good, please be aware that any form of linting will fail.

A simple example of this can be found below:
```
main {
    // Use the BACK button on the Xbox 360 
    // controller as the toggle for the event
    if (event_press(XB360_BACK)) {
         combo_toggle = !combo_toggle;
    }
    
    // If toggle is activated run the command
    if(combo_toggle) {
         combo_run (turbo);
    }
}
 
combo turbo {
    // Press A
    set_val(XB360_A, 100);
    wait(50);
}
```

## Contributing
Pull requests are welcome for any scripts you have used or found useful. For major changes to existing scripts, please open an issue first to discuss what you would like to change and why.