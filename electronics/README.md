# WeatherStation Electronics

This document contains information for obtaining and wiring up the electronics in the Clear Creek Scientific Weather Station, including a [bill of materials](#bill-of-materials), [setting up the Raspberry Pi](#setting-up-the-raspberry-pi) and  [wiring the parts together](#wiring-diagram).

## Bill of Materials

### Standard Components

|Manufacturer|Model|Description|Quantity|Example|
|------------|-----|-----------|--------|-------|
|Raspberry Pi|Zero WH|Single-board computer with wireless and headers|1|https://www.microcenter.com/product/502843/raspberry-pi-zero-wh-with-pre-soldered-headers|
|Raspberry Pi|12.5 W|Micro USB Power Supply (or equivalent)|1|https://www.raspberrypi.com/products/micro-usb-power-supply/|
|Multiple|At least 32 GB|Micro-SD card|1|https://www.microcenter.com/product/675340/sandisk-32gb-ultra-sdxc-class-10-u1-flash-memory-card|
|Adafruit|BME280|Temperature, Humidity, and Pressure sensor|1|https://www.adafruit.com/product/2652|
|Adafruit|STEMMA QT/Qwiic JST SH 4-pin Cable 1 mm pitch with Female Sockets|Connector|1|https://www.adafruit.com/product/4397|


### Optional Components

|Manufacturer|Model|Description|Quantity|Example|
|------------|-----|-----------|--------|-------|
|Multiple|Mini HDMI to HDMI|Video cable to connect Raspberry Pi to PC|1|https://www.raspberrypi.com/products/standard-hdmi-a-male-to-mini-hdmi-c-male-cable/|
|Multiple|USB A to USB Micro B|USB converter to connect Raspberry Pi to standard PC keyboard|1|https://www.microconnectors.com/usb-a-female-to-usb-micro-b-male-2-0-adapter-otg/|
|Multiple|Female-to-female jumper wires|Optional: use instead of the STEMMA QT/Qwiic connector|4|https://www.adafruit.com/product/1950|

## Setting up the Raspberry Pi

The Raspberry Pi requires some setup before it is able to be used in the Clear Creek Scientific WeatherStation. General instructions for multiple types of Raspberry Pi can be found on the [official Raspberry Pi website](https://www.raspberrypi.com/documentation/computers/getting-started.html). Specific instructions for the WeatherStation follow:

Perform the following steps:

* [Install an Operating System on the SD Card](#install-an-operating-system-on-the-sd-card)
* [Setup External Keyboard and Monitor](#setup-external-keyboard-and-monitor)
* [Plug in the Power Cord](#plug-in-the-power-cord)
* [Setup SSH](#setup-ssh)
* [Customize settings](#customize-settings)
 
### Install an Operating System on The SD Card

#### Using Windows as Host

#### Using Linux as Host


### Setup External Keyboard and Monitor

This step is is technically optional, but makes customization of the Raspberry Pi easier to perform. You will need an extra PC keyboard and monitor plus the optional adapters mentioned in the bill of materials above. Use the HDMI adapter to connect the mini-HDMI port on the Raspberry Pi Zero to the HDMI port on the PC monitor. Use the USB adapter to connect one of the USB micro B ports to the external keyboard monitor. The other USB micro B port will be used with the power adapter to power on the Raspberry Pi Zero.
 
### Plug in the Power Cord

If you haven't already done so, plug in the power adapter and connect the USB micro B cable to the second USB micro B port on the Raspberry Pi. You should see a green LED start to blink on the Pi. If you connected and external monitor to the Pi, you should see information on the screen as the Pi boots up. If you don't have a monitor, wait approximately two minutes to allow the Pi to start.

### Setup SSH

This step is needed to install the [WeatherStation software](https://github.com/ClearCreekSci/WeatherStation/tree/main/software), but is also necessary if you decide to not connect an external keyboard and monitor to the Raspberry Pi Zero.

#### Using Windows as Host

##### Using PuTTY

##### Using WSL

#### Using Linux as Host


### Customize Settings


## Wiring Diagram

The two diagrams below indicate how the pins on the Raspberry Pi Zero should be connected to the pins on the Adafruit BME280. The first diagram shows how to connect the two boards using the Adafruit STEMMA QT/Qwiic cables. The second diagram shows how to connect the two boards using 4 female-to-female jumper wires.

### With Adafruit STEMMA QT/Qwiic Cable
```
-----------------------------------

                 +---------------------------------------+
                 |               BME280                  |
                 +-----+                           +-----+ 
  |--------------+ GND | black              yellow | SCK +
  |          +---+ VIN | red                  blue | SDI +
  |       +--|---+ SDI | blue                  red | VIN +
  |    +--|--|---+ SCK | yellow              black | GND +
  |    |  |  |   +-----+                           +-----+
  |    |  |  |   |                                       |
  |    |  |  |   |                                       |
  |    |  |  |   |       V   3   G   S   S   S           |
  |    |  |  |   |       I   V   N   C   D   D   C       |
  |    |  |  |   |       N   O   D   K   O   I   S       |
  |    |  |  |   |       o   o   o   o   o   o   o       |
  |    |  |  |   +---------------------------------------+
  |    |  |  |
  |    |  |  |
  |    |  |  |                           
  |    |  |  |                          
  |    |  |  |                            
  +----|--|--|----------------------------+
       |  |  |                            |
       |  |  |                            |
       |  |  |      +----------------+    |
       |  |  +------|o 1 3.3v  5v 2 o|    |
       |  +---------|o 3 SDA   5v 4 o|    |
       +------------|o 5 SCL  GND 6 o|----+
                    |o 7          8 o|
                    |o 9         10 o|
                    |o 11        12 o|
                    |o 13        14 o|
                    |o 15        16 o|
                    |o 17        18 o|
                    |o 19        20 o|
                    |o 21        22 o|
                    |o 23        24 o|
                    |o 25        26 o|
                    |o 27        28 o|
                    |o 29        30 o|
                    |o 31        32 o|
                    |o 33        34 o|
                    |o 35        36 o|
                    |o 37        38 o|
                    |o 39        40 o|
                    +----------------+
```


### With female-to-female jumper wires
```
         +---------------------------------------+
         |               BME280                  |
         +-----+                           +-----+ 
         + GND | black              yellow | SCK +
         + VIN | red                  blue | SDI +
         + SDI | blue                  red | VIN +
         + SCK | yellow              black | GND +
         +-----+                           +-----+
         |                                       |
         |                                       |
         |       V   3   G   S   S   S           |
         |       I   V   N   C   D   D   C       |
         |       N   O   D   K   O   I   S       |
         |       o   o   o   o   o   o   o       |
         +-------+-------+---+-------+-----------+
                 |       |   |       |
                 |       |   |       |
                 |       |   |       |
                 |       |   |       |
       +---------+       |   |       |
       |                 |   |       |
       |  +--------------|---|-------+
       |  |              |   |
       |  |  +-----------|---+
       |  |  |           |
       |  |  |           +----------------+
       |  |  |                            |
       |  |  |      +----------------+    |
       +--|--|------|o 1 3.3v  5v 2 o|    |
          +--|------|o 3 SDA   5v 4 o|    |
             +------|o 5 SCL  GND 6 o|----+
                    |o 7          8 o|
                    |o 9         10 o|
                    |o 11        12 o|
                    |o 13        14 o|
                    |o 15        16 o|
                    |o 17        18 o|
                    |o 19        20 o|
                    |o 21        22 o|
                    |o 23        24 o|
                    |o 25        26 o|
                    |o 27        28 o|
                    |o 29        30 o|
                    |o 31        32 o|
                    |o 33        34 o|
                    |o 35        36 o|
                    |o 37        38 o|
                    |o 39        40 o|
                    +----------------+
                   Raspberry Pi Zero W or 
                    Raspberry Pi zero2 W
```
