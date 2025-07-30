# WeatherStation Electronics

This document contains information for obtaining and wiring up the electronics in the Clear Creek Scientific Weather Station, including a [bill of materials](#bill-of-materials), [setting up the Raspberry Pi](#setting-up-the-raspberry-pi) and  [wiring the parts together](https://github.com/ClearCreekSci/WikiBase/wiki/raspberry_pi_zero_to_bme280_wiring).

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

#### With Windows as Host

#### With Linux as Host


### Setup External Keyboard and Monitor

This step is is technically optional, but makes customization of the Raspberry Pi easier to perform. You will need an extra PC keyboard and monitor plus the optional adapters mentioned in the bill of materials above. Use the HDMI adapter to connect the mini-HDMI port on the Raspberry Pi Zero to the HDMI port on the PC monitor. Use the USB adapter to connect one of the USB micro B ports to the external keyboard monitor. The other USB micro B port will be used with the power adapter to power on the Raspberry Pi Zero.
 
### Setup SSH on Host

This step is needed to install the [WeatherStation software](https://github.com/ClearCreekSci/WeatherStation/tree/main/software) at a later time, but it is also necessary if you decide to not connect an external keyboard and monitor to the Raspberry Pi Zero.

#### With Windows as Host

Windows doesn't come with a built-in SSH client, so one needs to be installed. We suggest either downloading and install [Putty](https://www.putty.org/) or activating the Windows Subsytem for Linux (WSL) to use the native SSH client contained therein.

##### Using PuTTY

##### Using WSL

#### With Linux as Host

### Plug in the Power Cord

If you haven't already done so, plug in the power adapter and connect the USB micro B cable to the second USB micro B port on the Raspberry Pi. You should see a green LED start to blink on the Pi. If you connected and external monitor to the Pi, you should see information on the screen as the Pi boots up. If you don't have a monitor, wait approximately two minutes to allow the Pi to start.


### Customize Settings


