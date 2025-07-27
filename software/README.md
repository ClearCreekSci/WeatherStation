# WeatherStation Software

The Clear Creek Scientific weather station requires the following to be installed:

* An operating system for the Raspberry Pi
* Clear Creek Scientific Bluetooth GATT service software

## Raspberry Pi Operating System



### For Windows

Visit the official [Raspberry Pi "getting started" page](https://www.raspberrypi.com/documentation/computers/getting-started.html) and follow the instructions there.

### For Linux

         <li>Before running rpi-imager, inspect your Raspberry Pi to determine which version of the device you have.</li>
         <li>Run rpi-imager and select the device (Raspberry Pi Zero W or Raspberry Pi Zero 2 WH), operating system (Raspberry Pi OS Lite (32-bit), under Raspberry Pi OS (other)) and storage location (the micro SD card)</li>
         <li>When it asks &quot;Would you like to apply OS customisation settings?&quot;, select &quot;EDIT SETTINGS&quot; and configure the following:
             <ul>
                 <li>username and password</li>
                 <li>Wireless LAN SSID and password</li>
                 <li>Wireless LAN Country</li>
                 <li>Time zone</li>
                 <li>Keyboard layout</li>
             </ul>
         <li>Select &quot;SAVE&quot; and &quot;Yes&quot; to apply the settings. Then select &quot;YES&quot; to write the image to disk (it takes a few minutes).</li>
         <li>You will need to be either root when you run the program, or a sudo user so you can give rpi-imager access to write to the card</li>
         <li>Once the image is written, remove the sd card from the PC, place it in the Raspberry Pi and plug in the Raspberry Pi to start it.</li>
	</ol>

  	   <li>Configure ssh</li>
	   <li>Had to guess at IP address. If you execute the following command from another host on the network, it will help find it: <ul><li><code>sudo nmap -sP 192.168.200.0/24</code></li></li>

	 <p>References</p>
	 <ul>
		 <li>
			<a href="https://www.raspberrypi.com/documentation/computers/getting-started.html">Getting started on the official website</a>
		</li>
		<li>
			<a href="https://www.abelectronics.co.uk/kb/article/1094/i2c-part-4-programming-i2c-with-python">Programming i2c with Python</a>
		</li>
		<li>
			<a href="https://github.com/adafruit/Adafruit_CircuitPython_PCT2075">Installing Adafruit Circuit Python Libraries (PCT2075)</a>
		</li>
	 </ul>


## Clear Creek Software Bluetooth GATT Service
