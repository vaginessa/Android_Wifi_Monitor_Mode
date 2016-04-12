Hi All,

I am writing some notes about Monitor Mode on mobile,

N900 is the only phone that have a build in Wifi With Monitor Mode Support,
You can Install N900 image from here:

[pwnieexpress](https://www.pwnieexpress.com/)

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

Or

[Other Info](http://androidforums.com/threads/building-cm12-work-in-progress-join-in.891676/)

If all run ok, We will build a new Cyanogenmod + Kernel , 

Now,  lets build the with Monitor Mode support

3. Add Monitor Mode support in Cyanogenmod
Some kernels have mess up with ath Driver so here is my solution:

drivers/net/wireless/ath 
--> remove compat section from MakeFile (first 3 lines),

Copy & replace "main.c" and "ath.h" from "android_kernel_samsung_aries/tree/cm-11.0-bcmon/drivers/net/wireless/ath"

OR

Copy the driver from "android_kernel_samsung_aries/tree/cm-11.0-bcmon/drivers/net/wireless/ath"


drivers/net/wireless/bcmdhd --> Use Orginal Driver

drivers/net/wireless/rt2x00 --> Use Orginal Driver

drivers/net/wireless/rtl818x --> Use Orginal Driver

drivers/net/wireless/rtlwifi --> Use Orginal Driver

OR

Replacing /drivers/net/wireless/ath with the sources from original 3.0.31 kernel makes the
ath9k and ath9k_htc modules work, which is fairly interesting in terms of using it with nethunter.
The smdk4412 sources are messed somehow, if you reenable the ath9k Makefile.

4. How to Build Kernel Only

Build BootImage:

. build/envsetup.sh

lunch cm_n7100-userdebug 
or 
lunch cm_n7100-eng

mka bootimage

adb reboot bootloader

sudo heimdall flash --BOOT boot.img --no-reboot
(For Samsung Device, apt-get install heimdall )

or

sudo fastboot flash boot boot.img
(For Other Device, apt-get install fastboot )



https://blog.afoolishmanifesto.com/posts/replacing-your-cyanogenmod-kernel-for-fun-and-profit/

