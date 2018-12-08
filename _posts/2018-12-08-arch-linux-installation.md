---
layout: post
author: Jokke
title: Arch Linux installation
categories: [arch, linux, installation]
tags: [arch, linux, install, macbook]

---

# Few notes about the installation

## Partition: 

		  NAME	SIZE	TYPE			MOUNTPOINT
		---------------------------------------------------
		- sda1	550M	EFI System		/boot
		- sda2	16G 	Linux Swap  		SWAP
		- sda3	32G 	Linux filesystem 	/
		- sda4	64.5G	Linux filesystem	/home

		Filesystems: 
		
			- sda1 / EFI = FAT32
			- sda2 = Swap
			- sda3 = ext4
			- sda4 = ext4

## Time and Region

Europe/Helsinki

## Locale
	
Do not use FI locale! It turns parts of the terminal to Finnish. Very annoying feature. My locale.conf: 

 
`LANG=en_US.UTF-8` 

## CPU & FAN control & Battery

I found a great blog that I used with my installation:[https://mchladek.me/post/arch-mbp/](https://mchladek.me/post/arch-mbp/) 

Installed: 

- Powertop:
	- After install needs to run `powertop --calibrate`
	- Had to create powertop systemd service to: /etc/systemd/system/powertop.service

```
[Unit]
Description=Powertop tunings

[Service]
Type=oneshot
ExecStart=/usr/bin/powertop --auto-tune

[Install]
WantedBy=multi-user.target
```		 

	- Enable the service: 
	`systemctl enable powertop.service`	 

- Thermald: 
	- installed from pacman ("thermald")
	- enable the service:
	`systemctl enable thermald.service`

- Cpupower
	- Installed from pacman ("cpupower")	 
	- Config: /etc/default/cpupower

- Mbpfancontrol
	- Installed from yay ("mbpfan")
	- enable the service: 
	`systemctl mbpfan.service` 

## Software related issues:

### Steam

Enable multilib on /etc/pacman.conf, pacman -Syu -> pacman install steam
