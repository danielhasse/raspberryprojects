# Raspberry Pi Zero W - Headless Serverprojects

Setting up a headless server

## Download

- Go to Raspeberry website and grab the Raspeberry Pi Imager
- https://www.raspberrypi.org/downloads/

## Use Raspberry Pi Imager

1. Open the Raspberry Pi Imager
2. On the tab _"Operating System"_ _"Choose OS"_ and select _"Erase card"_
3. Go to _"SD Card"_ and _"Choose SD CARD"_ select the card you wish to erase and press _"Write"_
4. When you see _"Write Successful"_ you are ready to burn the Raspbian into the card.
5. On the tab _"Operating System"_ _"Choose OS"_ and select _"Raspberry Pi OS (other)"_ and then _"Raspberry Pi OS Lite(32bit)"_
6. Go to _"SD Card"_ and _"Choose SD CARD"_ select the card you wish to erase and press _"Write"_
7. After is finished you will see _"Write Successful"_

## Create SSH and Wireless Access

1. Open File Explorer and navigate to the drive where Raspberry pi OS is.
2. Create a newfile called SSH with no extensions - This will allow for SSH connections.
3. Create a newfile called wpa_supplicant.conf
4. OPen this and add the following and save the file:
```
country=ca
update_config=1
ctrl_interface=/var/run/wpa_supplicant

network={
 scan_ssid=1
 ssid="MyNetworkSSID"
 psk="MyPassword"
}
```
5. Now eject the card and pop into the Raspberry.

## Boot your RaspberryPi

1. Pop the card into the Raspberry Pi 
2. Connect usb cable to the left usb port on raspberry pi and to your usb port
3. Wait a cThe system will boot;
4. After booting open you can use putty or powershell to open a ssh connection
 - To use putty select SSH and set hostname as raspeberrypi.local and connect
 - To use powershell type 
 ```
 ssh pi@raspberry.local
 ```
 5. SSH into raspberrypi.local
  - username pi
  - password raspberry
 
 ### Change default password
 1. sudo passwd
 2. Change password for root
 ```
 sudo passwd root
 ``` 
 ### Configure a static ip address
 1. Edit the dhcpcd.conf file
 ```
 sudo nano /etc/dhcpcd.conf
 ```
 2. Add the following lines in the end of the file
 
 ```
 interface wlan0

static ip_address=192.168.0.25/24
static routers=192.168.0.1
static domain_name_servers=192.168.0.1
```
 
 
