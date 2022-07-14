---
title: Force Ubiquiti device adoption
date: 2022-07-14 22:30:00 +200
categories: [Networking, Ubiquiti]
tags: [network, ubiquiti, unifi, controller]
---

For whatever reason (controller issue maybe), I’ve had problems with new Unifi devices automatically showing up in the devices page on my controller (which is running on a Raspberry Pi 3b).  

I just bought a secondhand switch 16 port 150W PoE Unifi switch with this same issue occuring.  
What did it for me was to tell the device to contact my controller directly and ask for adoption. 

Like so:  

1. Factory reset the device
1. Obtain the IP of the device 
1. SSH into the device using default credentials (username: ubnt, password: ubnt) 
1. Execute command: ``set-default
``
1. Wait for the device to reboot 
1. SSH into the device again 
1. Execute command: ``
set-inform http://(IP-adress of the controller):8080/inform 
``
1. Log out of the device 

If you have the controller's *Devices page* open at the same time you should see the device appear as ready for adoption immediately.  

![Unifi Switch](/assets/unifiswitch.png)