## Motivation

This tool is used to streamline windows driver development for [WDK 7](http://www.microsoft.com/en-us/download/details.aspx?id=11800). I built this tool because the process of debugging windows
drivers is horrendous - at least for me. The flow for driver debugging currently goes like this:

1. Boot development VM
2. Compile windows driver
3. Manually move driver components to `C:\windows\system32`
4. Reboot 
5. Repeat 1


The whole process takes at least 5 minutes each time I want to debug a device driver. No bueno. 

Here's the process I hope to accomplish with this tool:

1. Navigate to source directory for device driver on dev computer
2. Build with `wdt build`
3. Repeat 2


WDT would handle all the heavy work by booting the VM, compiling, moving the source to `system32`, and providing console logging for `DbgPrint`.

## Features

- Boot, build, and copy target device driver
- Console logging for DgbPrint



## Requirements

- [node.js](nodejs.org)
- [WDK 7](http://www.microsoft.com/en-us/download/details.aspx?id=11800)
- VMWare Fusion
- SSH Server for Windows 
- Mac OSX
