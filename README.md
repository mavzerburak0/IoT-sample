# IoT-sample
#### IoT Lab for ICS

This repository is prepared for I600 Introduction to Computers and Informatics Course in Tallinn University of Technology.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

## Prerequisites

* Python 3.x
* Wemos ESP32
* Jumper Cables

## Running

First clone the repository to your computer via Git. Following commands are for Linux and Mac. Note that the codes are in src/ folder.


git clone https://github.com/mavzerburak0/iot-led.git
cd iot-led/src
On your machine

Run main.py like

python main.py
then browse to http://localhost:8080/

On WEMOS

Run following command:

sudo ampy -p /dev/ttyUSB0 put main.py 
Troubleshooting

## Resetting Device

If for any reason your device is struct, you may need to reset and reflash it.

Sample instructions do accomplish it are below for different chipsets:

esp32:

First download Firmware from http://micropython.org/download#esp32 and then

sudo esptool.py -p /dev/ttyUSB0 -b 460800 erase_flash
sudo esptool.py -p /dev/ttyUSB0 -b 460800 write_flash --flash_mode dio 0x1000 esp32-*.bin
esp8266:

wget http://micropython.org/resources/firmware/esp8266-20170612-v1.9.1.bin
sudo esptool.py -p /dev/ttyUSB0 -b 460800 erase_flash
sudo esptool.py -p /dev/ttyUSB0 -b 460800 write_flash 0 esp8266-*.bin
