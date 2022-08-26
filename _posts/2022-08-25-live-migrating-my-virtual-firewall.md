---
title: Live-migrating my virtual firewall
date: 2022-08-25 12:00:00 +200
categories: [Virtualization, Proxmox]
tags: [proxmox, homelab, pfsense, cluster]
---

# Hasttag thisiscool
I have been using pfSense as a virtual firewall for a long time and it has been great.
Having a Proxmox cluster allows me to migrate machines when I need to perform maintenance and for example reboot my Proxmox node.
I dont' have any shared storage (with enough performance to be of any use) for my VMs and containers, but I found that I can still live migrate machines from one node to another - it just takes a while.

This is all pretty standard for virtualization, but it has just been really easy to set up in Proxmox. And it just works.

I just really love that I can live migrate my pfSense firewall to another node only dropping one ping!

![Migrating in Proxmox](/assets/proxmoxmigrate.png)