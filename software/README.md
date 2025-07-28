# WeatherStation Software

The Clear Creek Scientific weather station requires the Clear Creek Scientific Bluetooth GATT service software to be installed on the Raspberry Pi before connecting to the weather station to your Android phone. You will need to [install an operating system on the Raspberry Pi](https://github.com/ClearCreekSci/WeatherStation/tree/main/electronics/#setting-up-the-raspberry-pi) before you can install the GATT service software.

To install the GATT service software, do the following:

* Download and extract the Clear Creek Scientific WeatherStation code
  * Navigate to the [WeatherStation main page](https://github.com/ClearCreekSci/WeatherStation/tree/main)
  * Click on the green "Code" button and select "Download ZIP" from the bottom of the menu
  * Extract the files from the ZIP archive using your favorite decompression software

## For Windows

  TODO:

## For Linux

* Use the scp command to copy the following files from the archive's "software" folder to the "pi" user's home directory on the Raspberry PI (you'll be asked for the password):
  * `> scp install_DataStation.sh pi@<IP address for PI>:/home/pi`
  * `> scp v1.0.0_DataStation_Install_Bundle.zip pi@<IP address for PI:/home/pi`
* SSH into the Raspberry PI (you'll be asked for the password):
  * `ssh pi@<IP address for PI>`
* Run the install script as root, passin the install bundle as a parameter:
  * `sudo ./install_DataStation.sh v1.0.0_DataStation_Install_Bundle.zip`
* Verify the script finishes successfully


