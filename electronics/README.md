# WeatherStation Electronics

This document contains information for obtaining and wiring up the electronics in the Clear Creek Scientific Weather Station, including a [bill of materials](#bill-of-materials), [setting up the Raspberry PI](#setting-up-the-raspberry-pi) and  [wiring the parts together](#wiring-diagram).

## Bill of Materials

|Manufacturer|Model|Description|Quantity|Example|
|------------|-----|-----------|--------|-------|
|Raspberry Pi|Zero WH|Single-board computer with wireless and headers|1|https://www.microcenter.com/product/502843/raspberry-pi-zero-wh-with-pre-soldered-headers|
|Raspberry Pi|12.5 W|Micro USB Power Supply (or equivalent)|1|https://www.raspberrypi.com/products/micro-usb-power-supply/|
|Multiple|At least 32 GB|Micro-SD card|1|https://www.microcenter.com/product/675340/sandisk-32gb-ultra-sdxc-class-10-u1-flash-memory-card|
|Adafruit|BME280|Temperature, Humidity, and Pressure sensor|1|https://www.adafruit.com/product/2652|
|Adafruit|STEMMA QT/Qwiic JST SH 4-pin Cable 1 mm pitch with Female Sockets|Connector|1|https://www.adafruit.com/product/4397|
|Multiple|Female to female jumper wires|Optional: use instead of the STEMMA QT/Qwiic connector|4|https://www.adafruit.com/product/1950|

## Setting up the Raspberry PI

TODO: Describe how to access the Raspberry Pi through connected monitor and keyboard OR through ssh. Refer to installing the OS in the software section. We mostly want help the consumer get familiar with using the Raspberry Pi here. We may also want to link to a CCS video demonstrating how to setup the PI for different environments (Windows/Linux host).

## Wiring Diagram

```
With Adafruit STEMMA QT/Qwiic Cable
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



With female to female jumper wires
----------------------------------

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
