---
title: My Proxmox journey begins [UPDATED]
date: 2022-09-21 18:00:00 +200
categories: [Virtualization, Proxmox]
tags: [virtualization, proxmox, opensource, hyperviser, homelab]
---

# Introduction: Moving from ESXi to Proxmox
Some time ago, now, I set up ESXi on an Intel NUC in my homelab - with a little help from a friend ;-)
I installed the first VM: pfSense. This is just an awesome firewall and I'll be sure to write about that in the future.

Anyway, I never really found ESXi was easy for me to work with. Specifically it was cumbersome to update and I had to roll-back the NIC driver after each update and it was almost necessary to have a monuitor attached.

I was never really happy with my backup solution. I had a Windows VM with VEEAM installed. No doubt, VEEAM is pretty much the best you can use, but for my homelab I just wanted something else. I don't have any extra Windows licenses, so I also had it set up in a non-activated VM with a limited lifespan to follow. And it didn't work with my pfSense - restore always failed and I never found out why.

So, let me try Proxmox I thought!

![PROXMOX](/assets/proxmoxlogo.png)

In an effort to collect snippets, code, configurations etc. on Github, rather than my blog, I decided to give this blog post an update and link to the repo in stead. It's also updated with a paragraph on how to add a QDevice to a two-node cluster to ensyre it is quorate.

My [Proxmox Basic Setup](https://github.com/mskydt/Cheat-Sheets/tree/main/Proxmox/Basic%20Setup) can be found here.