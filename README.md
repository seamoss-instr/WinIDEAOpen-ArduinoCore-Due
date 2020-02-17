# ArduinoCore for Arduino Due using WinIDEA Open
This is an example workspace for the WinIDEA Open IDE, enabling writing code and debugging on the Arduino Due.
By default, it is configured for use with the Segger J-Link debugger, but CMSIS-DAP and iTAG are also supported.
The Blink example is included in the Sketches folder.

## J-Link connection
If a 10-pin ARM Cortex debug connector is available, it can be connected to the unmarked connector on the Due as shown in [this tutorial](https://webcache.googleusercontent.com/search?q=cache:GNH8WMs6nVQJ:https://embeddedcomputing.weebly.com/segger-j-link-with-arduino-due8203.html+&cd=15&hl=sl&ct=clnk&gl=si&client=firefox-b-d).
Otherwise, there is a 4-pin SWD connector marked DEBUG next to the 10-pin connector, with the GND pin located furthest from the 10-pin connector.
Don't forget that the J-Link debugger also requires a 3.3V signal on the Vref pin (pin 1).

## How to start debugging
  - Build your program by pressing F7
  - Initialize your J-Link connection by clicking on *Segger -> J-Link Maintenance -> Connect J-Link*
  - Click on the Download button
  - If successful, the debugger stops in the Startup function. Now you can run your program (F5) or step through the code (F10), etc.
  
## Adding libraries
Library .c or .cpp files must be added to the build manager manually.
Put them into the Libraries folder on your filesystem, then right click the Libraries group in WinIDEA and select *Add files*. Add your .c and .cpp library files.
As long as the library .h files are in the Libraries folder, they should be found automatically by WinIDEA.
