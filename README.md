# ESP32-MicroPython
Flashing Micro Python onto ESP-32 and testing

## Ubuntu 20.04 LTS
 - Install [pySerial](https://pyserial.readthedocs.io/en/latest/pyserial.html)
 - Plug in ESP32 via USB and view `dmesg` output. You should see a line such as 
   > [ 7103.795526] usb 1-4: cp210x converter now attached to ttyUSB0

   which will tell you the serial port. Other lines you need should say
   
   > [ 7103.784622] usb 1-4: Manufacturer: Silicon Labs
   > [ 7103.784619] usb 1-4: Product: CP2102 USB to UART Bridge Controller
   
   give you the Chip CP2102 and Manufacturer, these are needed. Other similar boards may have a different serial port,manufacturer or chip.

 - Install [esptool.py](https://github.com/espressif/esptool) by following this [guide](https://randomnerdtutorials.com/flashing-micropython-firmware-esptool-py-esp32-esp8266/)
 - Install [VS Code](https://code.visualstudio.com/download) **not via snap!** but as a standard .deb package. Installing via snap will encounter problems getting pyMakr working (probably serial port not seen)
 - Install node.js VS Code extension
 - Install pyMakr VS Code extention

download firmware

esptool ---> flash

Install VS Code
Install node.js ext
install pymakr ext


