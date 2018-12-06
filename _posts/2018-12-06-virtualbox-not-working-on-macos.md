---
title: Virtualbox installation on MacOS
author: jokke
categories: [macOS, virtualbox]
tags: [macos, virtualbox, vm]

# Virtualbox not working on macos

When installing virtualbox to macOS, the installer won't finish without error. The virtualbox will be installed at the computer but it gives an error when trying to run vm:s.

![Error sceenshot](/assets/virtualbox-error.png)


To install virtualbox:

1. Download the image for the virtualbox from: https://www.virtualbox.org/
2. Run the installer and go trough the installation -> it exits with error.
3. Go to System preferences -> security & privacy -> there should be a block notification for Oracle America, Inc -> click allow.
4. Run the installer again 
5. It should work now!

![Security notification](/assets/virtualbox-error-allow.png)


