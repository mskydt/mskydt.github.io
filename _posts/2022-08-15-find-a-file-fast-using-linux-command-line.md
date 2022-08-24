---
title: Find a file fast using Linux command line
date: 2022-08-15 15:00:00 +200
categories: [Linux, Utilities]
tags: [linux, cli]
---

Use the app ``mlocate`` to find files easilly and fast on Linux commandline.

# Install and prep it
1. Install it with ``sudo apt update && sudo apt install mlocate -y``
1. Then force update the database with ``sudo updatedb``


# Search for a file
1. Find where **syslog** is mentioned: ``locate syslog``