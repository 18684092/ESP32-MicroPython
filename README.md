# ESP32-MicroPython
Flashing Micro Python onto ESP-32 and testing

## Ubuntu 20.04 LTS
 - Install [pySerial](https://pyserial.readthedocs.io/en/latest/pyserial.html)
 - Plug in ESP32 via USB and view `dmesg` output. You should see a line such as >cp210x ttyUSB0: cp210x converter now disconnected from ttyUSB0

 - Install [esptool.py](https://github.com/espressif/esptool) by following this [guide](https://randomnerdtutorials.com/flashing-micropython-firmware-esptool-py-esp32-esp8266/)
 - Install [VS Code](https://code.visualstudio.com/download) **not via snap!** but as a standard .deb package. Installing via snap will encounter problems getting pyMakr working (probably serial port not seen)
 - Install node.js VS Code extension
 - Install pyMakr VS Code extention

download firmware

esptool ---> flash

Install VS Code
Install node.js ext
install pymakr ext


