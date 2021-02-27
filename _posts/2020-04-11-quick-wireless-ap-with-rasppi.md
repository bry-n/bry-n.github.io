---
title: Wireless AP with RaspPi
permalink: /quick-wireless-ap-with-rasppi/
---
I needed an access point (ap) for some wireless testing.  I didn’t want to buy a wireless access point and had a few raspberry pi’s laying around.  After some research I stumbled across the RaspAP project on github. The instructions are pretty easy to follow.

Download the latest release of [raspbian buster lite](https://www.raspberrypi.org/downloads/raspbian/).
Read the [documentation](https://www.raspberrypi.org/documentation/installation/intsalling-images/README.md) if you need help with flashing the operating system onto an SD card.

Boot up your pi and run some updates:

`Sudo apt-get update && sudo apt-get upgrade`

`Sudo reboot`

Run raspi-config and change the wifi country localization option to your country

`Sudo raspi-config`

Download the RaspAP and run it using the dev install script.

`Curl -sL https://install.raspap.com | bash`

This is a very quick way to download and launch the installer

![](/assets/images/rasppi1.png)

Accept the defaults when prompted. When the script is finished you’ll be prompted for a reboot.

![](/assets/images/rasppi2.png)

Now you need to log in and config your new raspberry pi wireless access point. Don't forget to change the default username and passwords!

  * IP address: 10.3.141.1
  * Username: admin
  * Password: secret
  * DHCP range: 10.3.141.50-255
  * SSID: raspi-webgui
  * Password: ChangeMe

This is the dashboard
![](/assets/images/rasppi3.png)

Change all wireless access point settings from the hotspot menu
![](/assets/images/rasppi4.png)

Change the default username and password
![](/assets/images/rasppi5.png)

Resources:  
[https://github.com/billz/raspap-webgui](https://github.com/billz/raspap-webgui)
