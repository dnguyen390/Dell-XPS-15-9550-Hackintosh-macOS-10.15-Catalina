# Introduction
This repository contains my own hackintosh EFI configuration, using the clover bootloader. It is specifically built for the Dell XPS 15 9550 laptop, but may work with the Percision 5510 laptop with some minor tweaks and adjustments. It supports macOS Catalina 10.15.6. Up to two 4K@60Hz display connections are supported via type C with an adapter, and HDMI can also be connected. However, the internal display will turn off if three external displays are connected. This is a hardware limitation of the Intel iGPU, as it only has 3 pipelines for driving displays, one per display. Thunderbolt devices, such as external GPUs will have to be cold booted in order to properly work, and cannot be hot plugged. The existing Dell DW1830 wireless card is used to support WLAN and Airdop via Bluetooth. Nearly all native macOS touchpad gestures work, with the exception of Force Click not working. Sleep and wake functions work as they should. 

Battery life is about 5-8% worse on macOS compared to Windows 10. However, I am still getting around 7 hours of runtime with more than 12 chrome tabs open, and some applications running in the background.


<img src="https://github.com/dnguyen390/Dell-XPS-15-9550-Hackintosh-macOS-10.15-Catalina/blob/master/resources/icon.png">


# Tested Configuration
##  Hardware

* Model: Dell XPS 15 9550
* CPU: Intel Core i7-6700HQ
* Intel Graphic: HD 530
* Memory: Micron DDR4 2400MHz 16GB* 1  SK Hynix DDR4 2400MHz 8GB* 1
* Display: 4K Infinity Edge Touch Screen
* SSD: Samsung 970 Evo 250GB SSD
* Trackpad: Synaptics SYNA2393
* Battery: Dell 6GTPY 97Wh from the XPS 15 9570
* Audio: Realtek ALC298
* Touchscreen: Wacom WCOM488F
* WLAN + Bluetooth : DW1830

## Software

* BIOS: `1.5.0 - 1.11.2`
* Clover Boot Loader: `Build 5122`
* macOS Catalina: `10.15.0 - 10.15.6`
* Windows 10 Pro: `Version 1909`

# What Works
- [x] Wifi
- [x] Airdrop
- [x] FaceTime
- [x] iMessage
- [x] Handoff
- [x] Siri
- [x] iCloud
- [x] Find My Mac
- [x] App Store
- [x] 4K Touch Screen
- [x] Trackpad Gestures
- [x] Keyboard Shortcuts (Volume, Brightness, Play/Pause, Backlight, Print)
- [x] HDMI Port (4k@30Hz hot pluggable)
- [x] USB Type C Port (supports charging at 60w using Apple 87w USB C Power Adapter)
- [x] Thunderbolt 3 Devices (Tested with a Razer Core X, AMD RX 480 8GB)
- [x] Headphone Jack

# What Doesn't Work :(
- [ ] Killer 1535 (Must use Dell DW1830 in order to have WiFI, Bluetooth, and Airdrop support under macOS)
- [ ] Nvidia Geforce GTX 960m
- [ ] SD Card Reader (external USB ones work fine)
- [ ] Force Click
- [ ] FileVault (unable to boot on encypted volume, will get stuck on black screen)


# Known Bugs/Issues

* Trackpad very rarely will stop working. (fixed by rebooting the system.)
* iGPU graphics can be slightly choppy on a scaled external 4k monitor.
* Thunderbolt 3 Devices cannot be hot plugged, must be cold booted in order to work properly.
