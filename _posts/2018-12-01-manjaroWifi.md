---
layout: post
author: Jokke
title: Macbook air & manjaro wifi
categories: [manjaro, linux, wifi]
tags: [manjaro, linux, wifi, pacman]

---


# Using Macbook Air Wifi with Manjaro

With new linux installation my macbook wifi doesn't work OOB. Luckily I have an usb wifi-adapter that works in most linux distros. Here's the steps that I did to get the internal wifi working:

After installing manjaro on my computer, I inserted my wifi-adapter and connected to my wifi network.

- Opened terminal
- Updated my system with 
  `pacman -Syu`
- Checked my internal wifi-card model with `inxi -Nxxz` The output said that I have Broadcom BCM4360
- Checked my kernel version with `uname -a` it was version 4.14.
- Installed the correct driver with `pacman -S broadcom-wl` and I chose the right one for my kernel version: `linux414-broadcom-wl-6.30.223.271-61`

That's it. Probably going to have the same problem when I upgrade the kernel but now I know how to solve the problem.
