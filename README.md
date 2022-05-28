# PURPLEBoard BW16

![20220527_163800](https://user-images.githubusercontent.com/30090189/170722668-34a4be9d-adce-429b-aca4-43f00e78071a.jpg)

PURPLEBoard BW16 is a development board based on BW16 module. It has all features that BW16 offers, plus some aditional. In this repo you will find all the data you need to make this board, that include schematic, gerber files, etc. In adition, there are examples for all features that this PURPLEBoard BW16 variant offers.
## Features

* RTL8720DN
  * KM4 core
    * 200 MHz
    * 512 KB SRAM
    * TrustZone-M
    * FPU
    * DSP
  * KM0 core
    * 20 MHz
    * 64 KB SRAM
  * Wi-Fi
    * 802.11b/g/n/ac
    * 2.4GHz & 5GHz
  * Bluetooth
    * Bluetooth LE 5.0
  * Hardware
    * Interfaces: SD/SDIO, USB 2.0, SPI, UART, IR, SGPIO, I2C, USI, Audio DAC, Audio ADC, I2S, Timers
    * Operating voltage/Power supply: 3.0~3.6 V
* All GPIO pins breaks into two header rows
* UART CH340C chip
* User Buttons
  * BURN
  * RST
* Orange LED
* Micro USB UART port
* UART select switch

![20220527_163823](https://user-images.githubusercontent.com/30090189/170724443-bb44c223-ce93-4176-884c-e66b2f017f8a.jpg)

## Getting started

PURPLEBoard BW16 is a development board that can be programmed with AT commands and Arduino IDE.

### AT Commands

If AT commands are option, set RT0 set of switches to ON. For interfacing AT commands, use any of AT tools and set baudrate to 38400. For more info, imaging and AT commands list, check:
https://forum.amebaiot.com/t/resources-bw16-troubleshooting-guide/678

### Arduino IDE C/C++

If Arduino IDE is option, set RTL set of switches to ON. Add packet support to Preferences with:
https://github.com/ambiot/ambd_arduino/raw/master/Arduino_package/package_realtek.com_amebad_index.json
and install the boards. To upload a sketch to a board, you must enter BOOT mode. To do so, hold Burn pressed, press RST, release Burn.

![20220527_163834](https://user-images.githubusercontent.com/30090189/170725705-e39af36b-ba91-4c30-8705-5acd50597a85.jpg)


## Pinout

PURPLEBoard BW16 has a two-row header with 18 pins in total. Here you can find the boards diagram so check it out. As I mention, PURPLEBoard BW16 has all BW16 pins break out. That is the reason for the size of the board, besides 0805 components and soldering on one side only. To power additional sensors and modules, there are two GND pins and two power pins (5V and 3.3V). There is no VIN pin. GPIO pins are NOT 5V TOLERANT!!! Use some logic shifter, voltage divider, or OP-AMP when interfacing 5V devices.

* First Row
  * GPIO11
  * GPIO6
  * en
  * GPIO5
  * GPIO1 (LOG RX)
  * GPIO2
  * GPIO8
  * 5V
  * G
* Second Row
  * GPIO4 (TX0)
  * GPIO5 (RX0)
  * GPIO12
  * GPIO3
  * GPIO10
  * GPIO0 (LOG TX)
  * GPIO7
  * 3V3
  * G

## PROS

* LED
* WiFi 2.4GHz&5GHz
* Bluetooth 5.0 BLE
* UART micro USB
* Complete GPIO pinout

## CONS

## Dimensions

Dimensions of this board are 28x60mm. The hight is 7mm (without headers).

## Disclaimer

PURPLEBoard BW16 is an open-source development board. My small contribution to the community, that gave me so much. Feel free to use and modify as you want. It would be nice to add some credits if you do.
