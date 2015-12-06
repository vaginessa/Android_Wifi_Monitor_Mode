## **Any android device**

Cyanogenmod provides you with an option to build your own Cyanogen-build and integrated kernel building. With this you can compile an compatible kernel for your phone with desirable features. Here's a post that walks you through the process.

R̲e̲qu̲i̲r̲e̲m̲e̲n̲t̲s̲: Linux machine
USB cable
familiarity with basic commands
For Nexus 5

**## Approach 1:**

Kali NetHunter won't allow you to use inbuilt WiFi card to perform packet capture.
Moreover most mobile WiFi cards does not support promiscuous/monitor mode.
You need to use external WiFi card(such as Alfa card/Tp-link Wln722n),
connect to USB OTG on Nexus 5 for packet injection, then you're all set.

R̲e̲qu̲i̲r̲e̲m̲e̲n̲t̲s̲:
kali NetHunter
Root previliges
Host-mode support
USB OTG adapter cable
External WiFi card

**## Approach 2:**

No need to install Kali NetHunter/any custom ROM.
Android PCAP capture app lets user to capture WiFi packets.
It is developed by Kismet wireless.
It does not require Root previliges even.

R̲e̲qu̲i̲r̲e̲m̲e̲n̲t̲s̲:
Host-mode support
USB OTG adapter cable
External WiFi card
Other android devices,with Broadcom chipset

There's support only for Broadcom WiFi chipsets from this group. There's bcmon android app to capture network (works on stock but rooted-android). Only supported chipset (firmwares) are old BCM4329 and BCM4330 and there's been no development on official bcmon blog since July 2013. Other firmwares you may have to compile the drivers for it. You may have to compile the drivers manually for it.
Nexus 7(2012), Samsung galaxy S2 have BCM4330 whose internal wifi is capable of monitor mode. Also Motorola Xoom, Galaxy Tab, Nexus S, Nexus One have BCM4329 and known to support bcmon.

## **How To Add Monitor Mode in Any Android Device**

R̲e̲qu̲i̲r̲e̲m̲e̲n̲t̲s̲:
Host-mode support
USB OTG adapter cable
External WiFi card

1. I am using VirtualBox with fresh installed Ubuntu 14.04 LTS,

2. We need to Download Cyanogenmod prerequisites, follow this tut:


[Build Cyanogenmod](https://wiki.cyanogenmod.org/w/Build_for_jflte)

If all run ok, We will build a new Cyanogenmod + Kernel , now,  lets do the Monitor Mode Patch

3. Add Monitor Mode into Cyanogenmod





