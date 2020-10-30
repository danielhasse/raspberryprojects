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
