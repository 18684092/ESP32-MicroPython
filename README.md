# ESP32-MicroPython
Flashing Micro Python onto ESP-32 and testing

## Ubuntu 20.04 LTS
 - Run `sudo apt-get update` and `sudo apt-get upgrade` and make sure everything is up to date
 - Install [Python 3.7 or above](https://www.python.org/downloads/) and python3-pip
   `sudo apt-get install python3` and `sudo apt-get install python3-pip` 
 - Install [pySerial](https://pyserial.readthedocs.io/en/latest/pyserial.html)
 - Plug in ESP32 via USB and view `dmesg` output. You should see a line such as:

   > [ 7103.795526] usb 1-4: cp210x converter now attached to ttyUSB0

   ...which will tell you the serial port. Other lines you need should say:
   
   > [ 7103.784622] usb 1-4: Manufacturer: Silicon Labs

   > [ 7103.784619] usb 1-4: Product: CP2102 USB to UART Bridge Controller
   
   ...give you the Chip CP2102 and Manufacturer, these are needed in next steps. *Other similar boards may have a different serial port,manufacturer or chip*.

 - Install [esptool.py](https://github.com/espressif/esptool) by following this [guide](https://randomnerdtutorials.com/flashing-micropython-firmware-esptool-py-esp32-esp8266/) and flash the firmware to use MicroPython or this [MicroPython guide](https://micropython.org/download/esp32/). Note the MicroPython guide has links to the firmware. 
 - Install [VS Code](https://code.visualstudio.com/download) **not via snap!** but as a standard .deb package. Installing via snap will encounter problems getting pyMakr working (probably serial port not seen)
 - Install node.js VS Code extension
 - Install pyMakr VS Code extention
 - This [guide](https://randomnerdtutorials.com/micropython-esp32-esp8266-vs-code-pymakr/) explains the above 2 installs and how to connect to the ESP32 and run a simple script to flash an LED. This program is included in this repo as main.py
 - Practice connecting, running and changing the LED flash timing to get used to the process of making changes to scripts as you will probably encounter *quirks*. Sometimes you may need to restart VC Code, other times you have to wait longer than expected for a connection.
 - A quick [reference guide](https://docs.micropython.org/en/latest/esp32/quickref.html) is available for the ESP32 

 ### Useful to know
 At the command prompt within the pyMakr terminal (interactive REPL) getting the ESP32 MAC address can be found by the following code:

`import network`

`import ubinascii`

`mac = ubinascii.hexlify(network.WLAN().config('mac'),':').decode()`

`print mac`


