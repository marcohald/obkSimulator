# Intro

OpenBeken simulator. Written in SDL and OpenGL, currently works on Windows, but should be easy to port.

OpenBeken simulator allows you to draw a simple sketch (simplified schematic) of an IoT device and run OpenBeken on Windows on that simulated device.
You can place buttons, LEDs, relays, trimmers, power metering chips, interact with them (press buttons etc) and check how OpenBeken would behave on such device.
This allows you to develop OpenBK configurations and scripts easily, even without getting a real device.

Features:
- load and save sketches (JSON format) along with a simulated BK7231 flash memory dump (bin format; contains config, LittleFS, etc)
- draw a circuit like you'd draw in Cadsoft Eagle
- place and use buttons (they are simulated on voltage levels, so all Click, Double Click, Hold Start, Hold Release etc OBK events are working)
- place relays/bulbs that you can control with buttons or OBK panel or scripts
- whole OBK HTTP panel works on windows (as a HTTP server on port 80), the Javascript Web App also works, you basically get OBK device on Windows
- place single color, CW (CCT), RGB and RGBCW strips and simulate their behaviour 
- use Tasmota Device Groups on Windows (fully functional, simulated OBK device can talk to real Tasmota/Beken devices on your network)
- send GET packets with SendGET command (fully functional, your Windows OBK sim can send HTTP GET to any server)
- and more....

# Basic usage
Run the simulator executable. An SDL Window will open with your device simplified sketch (WiFi module and some peripherals), also an OpenBeken HTTP server will run on port 80 on your local machine, so you can access your virtual OBK device by entering "localhost" or your local IP in the web browser. Note that you need to have port 80 not in use for that purpose, so stop services like Apache/Xampp, etc, before running OBK sim.

Now you can do two things:
- you can play around with Web interface, scripts, etc, just like on any other physical device
- you can change the simulated hardware in the Simulator window, add objects (relays, bulbs, LEDs, buttons), connect them with wires and script them anyway you want in Web panel

Your current scene can be easily saved and loaded, just make sure to save manually after making changes to device flash memory - by default, they are NOT saved. To manage virtual devices, use FILE menu:
- qqq
- qqq
- qqq
- qqq

# Compiling




