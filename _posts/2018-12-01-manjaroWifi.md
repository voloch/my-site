---
layout: post
author: Jokke
title: Macbook air & manjaro wifi
categories: [manjaro, linux, wifi]
tags: [manjaro, linux, wifi, pacman]

---


# Using Macbook Air Wifi with Manjaro

With new linux installation my macbook wifi doesn't work OOB. Luckily I have an usb wifi-adapter that works in most linux distros. Here's the steps that I did to get the internal wifi working:

After installing manjaro on my computer, I inserted my wifi-adapter adn connected to my wifi network.

Opened terminal
Updated my system with 
<code>pacman -Syu</code>
Checked my internal wifi-card model with <code>inxi -Nxxz</code>. The output said that I have Broadcom BCM4360
Checked my kernel version with <code>uname -a</code> it was version 4.14.
Installed the correct driver with <code>pacman -S broadcom-wl</code> and I chose the right one for my kernel version: <code>linux414-broadcom-wl-6.30.223.271-61</code>

That's it. Probably going to have the same problem when I upgrade the kernel but now I know how to solve the problem.
