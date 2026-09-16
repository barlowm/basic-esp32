# basic-esp32
Simple test system of new ESP34 single board computer (SBC) (well technically the "ESP34" is a "[System on a Chip](https://en.wikipedia.org/wiki/System_on_a_chip)" (SoC)) with display

[Board Specs](https://www.lcdwiki.com/2.8inch_ESP32-32E_Display)
[Waveshare Guide](https://docs.waveshare.com/ESP32-S3-Touch-LCD-2.8)
[Instructables Quick Start Guide](https://www.instructables.com/Quick-Start-Guide-for-ESP32-S3-28inch-Capacitive-T/)


Development environment:
* [Arduino IDE](https://support.arduino.cc/hc/en-us/articles/360019833020-Download-and-install-Arduino-IDE)
* Standard download and install procedure.
* Run IDE upon install completion
* Allow access through Windows Defender Firewall
* Allow all SW installs during installation

https://espressif.github.io/arduino-esp32/
https://espressif.github.io/arduino-esp32/package_esp32_index.json
https://docs.espressif.com/projects/arduino-esp32/en/latest/installing.html

## Software Setup
* Open the Arduino IDE, go to **File > Preferences > Settings**, and paste the official ESP32 board URL into the Additional Board Manager URLs field.
Navigate to **Tools > Board > Boards Manager**, search for esp32, and install the package by `Espressif`.
* Plug your 2.8-inch board into your PC using a USB cable that supports data transfer.
Select your specific board model (such as ESP32 Dev Module or ESP32S3 Dev Module depending on your exact variant) and choose the correct COM Port under the Tools menu.

## Required Libraries
* Install the `TFT_eSPI` library via **Sketch > Include Library > Manager Libraries**  to drive the onboard 320x240 LCD.
* Configure the `User_Setup.h` file inside the `TFT_eSPI` library folder to match the specific display driver (typically ILI9341 or ST7789) and the correct SPI/backlight GPIO pins wired on your board variant.Install touch and UI helper libraries like XPT2046_Touchscreen or LVGL if you plan to build interactive touch menus
