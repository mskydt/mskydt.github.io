---
title: Adding a UPS to my homelab
date: 2022-09-20 12:00:00 +200
categories: [Homelab]
tags: [proxmox, synology, raspberrypi opensource, homelab, nut]
---

# Introduction
My homelab is built for fun and learning, but also to power services for my home such as Home Assistant. The fun and learning part has resulted in a virtual firewall. So, I need to take care of my Proxmox cluster and keep it operational, otherwise internet will not work in my home. That's not good. So in a sense, my homelab is a "production deployment". Then there are the services I rely on and will come to rely on when built. I want to keep them safe if power outages should occur.

![Batteries](/assets/batteries.jpg)

# Requirements
My fiber modem is not in my rack with the rest of my home lab. So keeping internet running in case of a power outage is not a requirement. I "just" want my homelab to shut down gracefully after a short while. No need for hours of run-time on the battery.

I have a Conbee II USB stick for Zigbee that I'm going to use for a new install of Home Assistant. The last VM broke somthing after ... a power outage. Apparently it's a bit senstive like that.

# The software solution
[Network UPS Tools a.k.a. "NUT"](https://networkupstools.org/) is open source and supports many diferent UPS brands. It is very configurable albeit a bit difficult to get working. There are, however, great guides and Youtube videos that have helped me a lot getting it working.

![NUT Logo](/assets/nutlogo.png)

# Selecting the hardware
My homelab currently uses about 60 watts which made the following a good choice.
- **Bluewalker PowerWalker VI 850 SHL 850VA / 480W 2x Type F Outputs**
It supports NUT and has two normal power outlets with no need for additional investments in a cable converter or new power strip for my rack.

![Powerwalker UPS](/assets/powerwalkerups.png)

# Here's what you need to get started
Visit my GitHub Cheat-Sheet repo where you can find [my implementation of Network UPS Tools](https://github.com/mskydt/Cheat-Sheets/tree/main/Tools%20and%20systems/Network%20UPS%20Tools%20-%20NUT) including rudimentary description and configuration files for the NUT server on a Raspberry Pi, NUT client for my Proxmox hosts and the NUT client configuration for my Synology Diskstation.
