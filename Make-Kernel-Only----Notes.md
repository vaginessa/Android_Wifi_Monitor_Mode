Add Lines:

For ATH9K Wireless:

~/kernel/samsung/smdk4412/drivers/net/wireless/KConfig

+source "drivers/net/wireless/ath/Kconfig"

~/kernel/samsung/smdk4412/drivers/net/wireless/Makefile
+obj-$(CONFIG_ATH_COMMON)        += ath/

For UAS Driver:

~/kernel/samsung/smdk4412/drivers/usb/storage/KConfig

-depends on USB && SCSI && BROKEN


Make Kernel:

make  CROSS_COMPILE=~/prebuilts/gcc/linux-x86/arm/arm-eabi-4.8/arm-eabi/bin/ ARCH=arm cyanogenmod_n7100_defconfig

make  CROSS_COMPILE=~/prebuilts/gcc/linux-x86/arm/arm-eabi-4.8/arm-eabi/bin/ ARCH=arm menuconfig

make  CROSS_COMPILE=~/prebuilts/gcc/linux-x86/arm/arm-eabi-4.8/arm-eabi/bin/ ARCH=arm mrprepr

make  CROSS_COMPILE=~/prebuilts/gcc/linux-x86/arm/arm-eabi-4.8/arm-eabi/bin/ ARCH=arm  clean

make  CROSS_COMPILE=~/prebuilts/gcc/linux-x86/arm/arm-eabi-4.8/arm-eabi/bin/ ARCH=arm

Make Kernel Image:

. build/envsetup.sh

lunch cm_n7100-userdebug or lunch cm_n7100-eng

mka bootimage