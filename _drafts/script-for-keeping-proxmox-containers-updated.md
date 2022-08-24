---
title: Script for keeping Proxmox containers updated
date: 2022-08-12 12:00:00 +200
categories: [Virtualization, Proxmox]
tags: [proxmox, homelab, bash, script]
---

Github user Vzamora created a great collection of scripts and descriptions for Proxmox called [Proxmox Cheatsheet](https://github.com/vzamora/Proxmox-Cheatsheet/blob/main/General%20Proxmox%20Setup%20and%20Notes).

A specific script called [XC Updater - CronTab.](https://github.com/vzamora/Proxmox-Cheatsheet/blob/main/General%20Proxmox%20Setup%20and%20Notes/LXC%20Updater%20-%20CronTab.md) is of interest for me.
This script traverses all LXC containers on the host and upgrades them. If a container is not running, it is startet, updated and stopped again. If it is running already, it's just updated.

# I would like more functionality
I would like a bit more functionlity, and that's what I will try to create:
1. I need a way to list containers the script should skip
1. 