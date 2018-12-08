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
