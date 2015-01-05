torbox
======

A tor box from WT3020H box

# Installation

* Buy a WT3020 box and upgrade its firmware

I bought http://www.aliexpress.com/item/New-2014-300Mbps-WT3020A-Multiprotocol-Portable-Mini-WIFI-Router-with-USB-data-line-Wireless-Router-wi/1643935906.html

You may choose some other box from the list here also: http://wiki.openwrt.org/toh/nexx/wt3020
The supported Openwrt images are also listed there.

Plug RJ45 cable to the LAN port of the box. The default web interface will be at the adress 192.168.1.1. Open it 
with your browser. Choose a password for the root user. Update the firmware.

For the WT3020H version, the firmware is openwrt-ramips-mt7620n-wt3020-squashfs-8M-factory.bin that is downloaded from http://onionwrt.link/download/

Wait till your box rebooted. Then use the upgrade image to upgrade your firmware. 

* Set the LAN ip

After upgrading, you will be still able to ssh to the box from the ip 192.168.1.1. You may need to set a password, if you didn't keep the settings, for the root user.

Go to Network -> Interfaces tab and Edit LAN interface. Choose an IPv4 address. I choose 192.168.10.1 for not to comfuse with the ADSL router's default range.

* Set the wireless

Network -> WiFi menu and the enable it

* Plug the box to the ADSL modem

At the box, plg the cable to WAN inerface and at the ADSL modem to its one of the LAN interface. Boot power up the machine, ssh to the 192.168.10.1 or whatever IP address you gace to the LAN interface.

* Download and install the script

Test your internet connectivity

```
# ping www.google.com
```

Download the script and run it

```
# wget http://onionwrt.us.to/install
# sh install
```

After the script ends, you will loose your wireless connection, reconnect it. Your ssh session will be back.

* Connect to the OpenWrt ssid and check your tor connectivitiy

Try the addresses 

https://check.torproject.org/ and http://www.whatismyip.com/

