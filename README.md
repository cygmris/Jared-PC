# Asrock Phantom Gaming ITX / 9900K / Sapphire RX570
* Version - 10.15
* The kexts have been updated to support MacOS Catalina! Do a fresh install of all kexts to be safe. (Including removing those added to other folders not in `EFI`)

##### Table of Contents
* [Images](#images)
* [PC Parts](#parts)
* [BIOS Settings](#bios)
* [What Works](#what-works)
* [Features Still Being Tested](#still-testing)
* [Installation](#installation)
* [Motivation](#motivation)

<a name="images"></a>

## Images

![About this Mac](https://github.com/kcunanan/Jared-PC/blob/master/images/catalina-10-15-screenshot.png?raw=true)

![Desktop Screenshot](https://github.com/kcunanan/Jared-PC/blob/master/images/neofetch-catalina.png?raw=true)

<div align="center">
  <img src="https://github.com/kcunanan/Jared-PC/blob/master/images/catalina-geekbench.png?raw=true">
</div>


### PC: Photos out of Date
![PC Case - Side Closed](https://github.com/kcunanan/Jared-PC/blob/master/images/closed-side-pc.jpg?raw=true)
![PC Case - Front](https://github.com/kcunanan/Jared-PC/blob/master/images/front-pc.jpg?raw=true)
![PC Case - Back](https://github.com/kcunanan/Jared-PC/blob/master/images/back-pc.jpg?raw=true)
![PC Case - Open Side Left](https://github.com/kcunanan/Jared-PC/blob/master/images/open-pc-side-left.jpg?raw=true)
![PC Case - Open Side Right](https://github.com/kcunanan/Jared-PC/blob/master/images/open-side-pc-right.jpg?raw=true)

<a name="parts"></a>

## Parts
* Intel Core i9-9900k
* ASRock Z390 Phantom Gaming-ITX/AC
* AMD Sapphire RX570
* 16gb (2 x 8gb) Corsair Vengeance LPX DDR4 3200MHz
* Noctua NH-DL9
* Samsung 970 EVO 500gb - NVMe PCIe M.2.
* WD Blue 3D NAND 1TB PC SSD
* Broadcom BCM94352Z (Dell DW1560)
* DA2 Streacom Mini-ITX Case

<a name="bios"></a>

## BIOS
* Graphics -> iGPU Multi-Monitor enabled

<a name="what-works"></a>

## What Works
* iGPU for Accelerated Graphics
* Airdrop
* Audio
* USB 3.0 Speeds
* Bluetooth
* Wi-Fi (2.4 and 5ghz)
* Ethernet
* Sleep (have not had issues for the past few months! As of 10/26/2019)
* Shutdown
* Front Panel USB-C
* Thunderbolt 3 (for graphics or for usb when powered on with it)

<a name="still-testing"></a>

## Still Testing
* iMessage

<a name="installation"></a>

## Installation
* FYI - the only important folder here is the `EFI` everything else is supplementary. Will update eventually. If you'd like to know sooner, feel free to submit an issue with specific questions about the installation process so I know that it's needed by someone.

### config.plist
* Be sure to generate a new `Serial Number` and `SmUUID` for the SMBIOS

### Motherboard
Currently using bios 1.50 with `Fix AsRock Z390 BIOS DSDT Device(RTC) bug` fix

Change these settings in the BIOS
* Advanced > Chipset Configuration > VT-d -> Disabled
* Advanced > USB Configuration > XHCI Hand-off -> Enabled

### Wi-Fi / Bluetooth 
* ~~I replaced the stock Asrock Wi-Fi / BT card with a BCM94350ZAE WiFi / Bluetooth Chip. (create an issue if you'd like more documentation on this process)~~
* [Moved to this card](https://www.ebay.com/itm/252319175707) - I've tested 5ghz and BT on both MacOS and Windows and each works without a problem as of **6/07/2019**

<a name="motivation"></a>

## Why I Decided to Build a Hackintosh
My reasons for using macOS are pretty straightforward: I am a developer that loves MacOS for the look and feel of the operating system, and also MacOS' development environment. I started to get frustrated because my 2014 MacBook Pro felt sluggish and ran hot since I run `Docker` with most of my development. I had been really excited with the new 2018 Mac Mini, but I heard a lot of criticism about the lack of power, below-average thermals, and limited customizability. For around $1200, it definitely seemed like I could spend my money more effectively, so I decided to do more research.

Before coming to the conclusion that I should build a Hackintosh, I experimented with various alternatives that could solve my dilemma. I tried Linux (Elementary, Deepin, Ubuntu, Mint) from time to time, but frankly it just isn't my cup of tea yet. I considered trying to replace my MacBook's hard drive with an NVMe drive to potentially help, but that came with it's own problems and I wasn't sure it was worth it. I even bought (and eventually returned) a used 2012 Mac Mini and replaced the hard drive with an SSD. This worked out pretty nicely, but I was underwhelmed by the processing power and started to worry about how long that would last since I invested a good amount of $$ for something older than my MacBook Pro. At some point, I tried using VMs for MacOS, but it didn't feel smooth, and my hardware was still a bottleneck. I became really enthused with the idea of having a desktop Mac that was completely customizable, could look like a Mac, would be fairly future-proof, and could dual boot Windows primarily for gaming.

I hope this information helps someone out there!
