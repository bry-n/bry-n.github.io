---
title: 'Ubiquiti&#8217;s UniFi Controller on Linux'
permalink: /ubiquitis-unifi-controller-on-linux/
tags: Unifi
---
I recently purchased a UniFi Switch 8 60W for around $85 at Staples. You can read more about the switch here:  
https://www.ui.com/unifi-switching/unifi-switch-8/

I also use Ubiquiti's UniFi 802.11ac Dual-Radio PRO Access Point (UAP-AC-PRO-US).  Both the switch and the wireless ap require Ubiquiti’s UniFi Controller software. I decided to run the UniFi Controller on an Ubuntu Server 20.04 virtual machine. I wrote a simple bash script to automate the install of the controller software. The script can be downloaded from my github page.

https://github.com/bry-n/unifi  

The script will download and install everything needed to run Ubiquiti's UniFi Controller 5.13.29 on Ubuntu Server 20.04.

Ubiquiti offers a deb package and requires a few dependencies. The software requirements for 5.13.29 are as follows with full details linked below.

  * Linux: Ubuntu Desktop / Server 16.04; Debian 9 "Stretch"
  * At least Mongodb 3.6
      * 5.13.29 added support for Mongodb 3.6
  * Open jdk 8
      * 11 is not officially supported. I did not test running version 11.
  * Libssl1.0.0_1.0.2n-1ubuntu5.3_amd64.deb
      * Required dependency for mongodb 3.*. I found a reference to this in another script. I’ll reference below. 
      * Mongodb 3.* needs libssl1.0

[Unif-Requirements](https://help.ui.com/hc/en-us/articles/360012192813#unifi-requirements)  
[Unifi release notes for 5.13.29](https://community.ui.com/releases/UniFi-Network-Controller-5-13-29/d7647910-77a2-4e61-bbfe-389206f2d6ad)  
[libsssl 1.0.* reference](https://gist.github.com/davecoutts/5ccb403c3d90fcf9c8c4b1ea7616948d)
