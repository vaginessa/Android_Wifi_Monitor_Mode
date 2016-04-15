make  CROSS_COMPILE=~/prebuilts/gcc/linux-x86/arm/arm-eabi-4.8/arm-eabi/bin/ ARCH=arm cyanogenmod_n7100_defconfig
make  CROSS_COMPILE=~/prebuilts/gcc/linux-x86/arm/arm-eabi-4.8/arm-eabi/bin/ ARCH=arm menuconfig

[PAGE 1]                                                             
   								General setup  --->                                                                                                               
                                                                [*] Enable loadable module support  --->                                                                                              
                                                                [*] Enable the block layer  --->                                                                                                      
                                                                    System Type  --->                                                                                                                 
                                                                [ ] FIQ Mode Serial Debugger (NEW)                                                                                                    
                                                                    Bus support  --->                                                                                                                 
                                                                    Kernel Features  --->                                                                                                             
                                                                [ ] Build VMware Mobile Virtualization Platform modules (NEW)                                                                         
                                                                    Boot options  --->                                                                                                                
                                                                    CPU Power Management  --->                                                                                                        
                                                                    Floating point emulation  --->                                                                                                    
                                                                    Userspace binary formats  --->                                                                                                    
                                                                    Power management options  --->    

                                                                                                
                                                                -*- Networking support  --->    [ENTER]                                                                                                      
                                                                    Device Drivers  --->        [ENTER]

                                                                                                         
                                                                    File systems  --->                                                                                                                
                                                                    Kernel hacking  --->                                                                                                              
                                                                    Security options  --->                                                                                                            
                                                                -*- Cryptographic API  --->                                                                                                           
                                                                    Library routines  --->                                                                                                            
                                                                ---                                                                                                                                   
                                                                    Load an Alternate Configuration File                                                                                              
                                                                    Save an Alternate Configuration File                                                                                              
                                                                                                           

[PAGE 2]                              
                                                 --->               [--- Networking support]                                                                                                               
                                                                     Networking options  --->                                                                                                       
                                                               [*]   Amateur Radio support  --->                                                                                                    
                                                               <M>   CAN bus subsystem support  --->                                                                                                
                                                               <M>   IrDA (infrared) subsystem support  --->                                                                                        
                                                               <M>   Bluetooth subsystem support  --->                                                                                              
                                                               <M>   Bluetooth subsystem support(Tizen)  ---> 

                                                                                      
                                                               -*-   Wireless  --->   [ENTER]

                                                                                                                
                                                               <M>   WiMAX Wireless Broadband support  --->                                                                                         
                                                               <*>   RF switch subsystem support  --->                                                                                              
                                                               <M>   Plan 9 Resource Sharing Support (9P2000)  --->                                                                                 
                                                               <M>   CAIF support  --->                                                                                                             
                                                                                                      

[PAGE 3]

--- Wireless                                                                                                                         
                                                               <M>   cfg80211 - wireless configuration API                                                                                          
                                                               [ ]     nl80211 testmode command                                                                                                     
                                                               [ ]     enable developer warnings                                                                                                    
                                                               [ ]     cfg80211 regulatory debugging                                                                                                
                                                               [*]     enable powersave by default                                                                                                  
                                                               [*]     cfg80211 DebugFS entries                                                                                                     
                                                               [ ]     use statically compiled regulatory rules database                                                                            
                                                               [*]     cfg80211 wireless extensions compatibility                                                                                   
                                                               [*]   Wireless extensions sysfs files (NEW) 
                                                                                         
                                                               {M}   Common routines for IEEE802.11 drivers    
                                                                                     
                                                               [ ]   lib80211 debugging messages                                                                                                    
                                                               [ ]   Allow reconnect while already connected (NEW)      
                                                                            
                                                               <M>   Generic IEEE 802.11 Networking Stack (mac80211)  
                                                                              
                                                               [*]   PID controller based rate control algorithm                                                                                    
                                                               [*]   Minstrel                                                                                                                       
                                                               [*]     Minstrel 802.11n support                                                                                                     
                                                                     Default rate control algorithm (Minstrel)  --->                                                                                
                                                               -*-   Enable LED triggers                                                                                                            
                                                               [*]   Export mac80211 internals in DebugFS                                                                                           
                                                               [ ]   Select mac80211 debugging features  --->     

[PAGE 4]


						--->		[Generic Driver Options  --->]                                                                                                    
                                                               <*> Connector - unified userspace <-> kernelspace linker  --->                                                                       
                                                               <M> Memory Technology Device (MTD) support  --->                                                                                     
                                                               <M> Parallel port support  --->                                                                                                      
                                                               [*] Block devices  --->                                                                                                              
                                                               -*- Misc devices  --->                                                                                                               
                                                               < > ATA/ATAPI/MFM/RLL support (DEPRECATED)  --->                                                                                     
                                                                   SCSI device support  --->                                                                                                        
                                                               <*> Serial ATA and Parallel ATA drivers  --->                                                                                        
                                                               [*] Multiple devices driver support (RAID and LVM)  --->                                                                             
                                                               <M> Generic Target Core Mod (TCM) and ConfigFS Infrastructure  --->                                                                  
                                                               [*] Fusion MPT device support  --->                                                                                                  
                                                                   IEEE 1394 (FireWire) support  --->                                                                                               
                                                               <M> I2O device support  --->  

                                                                                                       
                                                               -*- Network device support  --->    [ENTER]   

                                                                                             
                                                               [*] ISDN support  --->                                                                                                               
                                                               < > Telephony support (NEW)  --->               




[PAGE 5]

  --- Network device support                                                                                                           
                                                               <M>   Intermediate Functional Block support                                                                                          
                                                               <M>   Dummy net driver support                                                                                                       
                                                               <M>   Bonding driver support                                                                                                         
                                                               <M>   EQL (serial line load balancing) support                                                                                       
                                                               <*>   Universal TUN/TAP device driver support                                                                                        
                                                               <M>   Virtual ethernet pair device                                                                                                   
                                                               <M>   ARCnet support  --->                                                                                                           
                                                               {M}   Generic Media Independent Interface device support                                                                             
                                                               {*}   PHY Device support and infrastructure  --->                                                                                    
                                                               [ ]   Ethernet (10 or 100Mbit) (NEW)  --->                                                                                           
                                                               -*-   Ethernet (1000 Mbit)  --->                                                                                                     
                                                               -*-   Ethernet (10000 Mbit)  --->                                                                                                    
                                                               < >   Token Ring driver support (NEW)  --->   
  
                                                                                     
                                                               [*]   Wireless LAN  --->   [ENTER]

                                                                                                    
                                                                     WiMAX Wireless Broadband devices  --->                                                                                         
                                                                     USB Network Adapters  --->                                                                                                     
                                                               [ ]   PCMCIA network device support (NEW)  --->                                                                                      
                                                               [*]   Wan interfaces support  --->                                                                                                   
                                                               [*]   ATM drivers  --->                              






[PAGE 6]

 --- Wireless LAN                                                                                                                     
                                                               <M>   Aviator/Raytheon 2.4GHz wireless support                                                                                       
                                                               <M>   Marvell 8xxx Libertas WLAN driver support with thin firmware                                                                   
                                                               [ ]     Enable full debugging output in the Libertas thin firmware module.                                                           
                                                               <M>     Marvell Libertas 8388 USB 802.11b/g cards with thin firmware                                                                 
                                                               <M>   Atmel at76c50x chipset  802.11b support                                                                                        
                                                               <M>     Atmel at76c506 PCI cards                                                                                                     
                                                               <M>     Atmel at76c502/at76c504 PCMCIA cards                                                                                         
                                                               <M>   Atmel at76c503/at76c505/at76c505a USB cards                                                                                    
                                                               <M>   Cisco/Aironet 34X/35X/4500/4800 PCMCIA cards                                                                                   
                                                               <M>   USB ZD1201 based Wireless device support                                                                                       
                                                               <M>   Realtek 8187 and 8187B USB support                                                                                             
                                                               <M>   Simulated radio testing tool for mac80211                                                                                      
                                                               [ ]   Enable WiFi control function abstraction (NEW)    
                                                                             
                                                               <M>   Atheros Wireless Cards  --->    [ENTER]  
                                                                                             
                                                               <M>   Broadcom 43xx wireless support (mac80211 stack)                                                                                
                                                               [ ]     Broadcom 43xx PCMCIA device support                                                                                          
                                                               [ ]     Broadcom 43xx debugging                                                                                                      
                                                               <M>   Broadcom 43xx-legacy wireless support (mac80211 stack)                                                                         
                                                               [ ]     Broadcom 43xx-legacy debugging                                                                                               
                                                                       Broadcom 43xx-legacy data transfer mode (DMA + PIO)  --->                                                                    
                                                               < >   Broadcom 4330 wireless cards support (NEW)                                                                                     
                                                               < >   Broadcom 4334 wireless cards support (NEW)                                                                                     
                                                               < >   Broadcom 4335 wireless cards support (NEW)                                                                                     
                                                               < >   Broadcom 4339 wireless cards support (NEW)                                                                                     
                                                               < >   Broadcom 4354 wireless cards support (NEW)                                                                                     
                                                               < >   Broadcom 43241 wireless cards support (NEW)                                                                                    
                                                               (/system/etc/firmware/fw_bcmdhd.bin) Firmware path (NEW)                                                                             
                                                               (/system/etc/wifi/bcmdhd.cal) NVRAM path (NEW)                                                                                       
                                                               <M>   IEEE 802.11 for Host AP (Prism2/2.5/3 and WEP/TKIP/CCMP)                                                                       
                                                               [*]     Support downloading firmware images with Host AP driver                                                                      
                                                               [*]       Support for non-volatile firmware download                                                                                 
                                                               <M>     Host AP driver for Prism2/2.5/3 in PLX9052 PCI adaptors                                                                      
                                                               <M>     Host AP driver for Prism2.5 PCI adaptors                                                                                     
                                                               <M>     Host AP driver for Prism2/2.5/3 PC Cards                                                                                     
                                                               <M>   Intel PRO/Wireless 2100 Network Connection                                                                                     
                                                               [*]     Enable promiscuous mode                                                                                                      
                                                               [ ]     Enable full debugging output in IPW2100 module.                                                                              
                                                               <M>   Intel PRO/Wireless 2200BG and 2915ABG Network Connection                                                                       
                                                               [*]     Enable promiscuous mode                                                                                                      
                                                               -*-       Enable radiotap format 802.11 raw packet support                                                                           
                                                               [*]       Enable creation of a RF radiotap promiscuous interface                                                                     
                                                               [ ]     Enable full debugging output in IPW2200 module.                                                                              
                                                               [ ]   Full debugging output for the LIBIPW component                             
                                                               < >   Intel Wireless WiFi Next Gen AGN - Wireless-N/Advanced-N/Ultimate-N (iwlagn)  (NEW)                                            
                                                                     Debugging Options  --->                                                                                                        
                                                               <M>   Intel Wireless WiFi 4965AGN (iwl4965)                                                                                          
                                                               <M>   Intel PRO/Wireless 3945ABG/BG Network Connection (iwl3945)                                                                     
                                                               <M>   Marvell 8xxx Libertas WLAN driver support                                                                                      
                                                               <M>     Marvell Libertas 8388 USB 802.11b/g cards                                                                                    
                                                               <M>     Marvell Libertas 8385 CompactFlash 802.11b/g cards                                                                           
                                                               <M>     Marvell Libertas 8385/8686/8688 SDIO 802.11b/g cards                                                                         
                                                               <M>     Marvell Libertas 8686 SPI 802.11b/g cards                                                                                    
                                                               [ ]     Enable full debugging output in the Libertas module.                                                                         
                                                               [*]     Enable mesh support                                                                                                          
                                                               <M>   Hermes chipset 802.11b support (Orinoco/Prism2/Symbol)                                                                         
                                                               [ ]     Support Prism 2/2.5 chipset                                                                                                  
                                                               [*]     Cache Hermes firmware on driver initialisation                                                                               
                                                               <M>     Hermes in PLX9052 based PCI adaptor support (Netgear MA301 etc.)                                                             
                                                               <M>     Hermes in TMD7160 based PCI adaptor support                                                                                  
                                                               <M>     Nortel emobility PCI adaptor support                                                                                         
                                                               <M>     Hermes PCMCIA card support                                                                                                   
                                                               <M>     Symbol Spectrum24 Trilogy PCMCIA card support                                                                                
                                                               <M>     Agere Orinoco USB support 
                                                                                                   
                                                               <M>   Ralink driver support  --->   [ENTER] 
                                                                                                 
                                                               <M>   Marvell WiFi-Ex Driver                                                                                                         
                                                               <M>     Marvell WiFi-Ex Driver for SD8787                                                                                            
                                                               < >   LGU IWLAN support (NEW)   













[UAS_Driver]

# 
# NOTE: USB_STORAGE depends on SCSI but BLK_DEV_SD may
#

#
# also be needed; see USB_STORAGE Help for more info
#
CONFIG_USB_STORAGE=y
# CONFIG_USB_STORAGE_DEBUG is not set
# CONFIG_USB_STORAGE_REALTEK is not set
# CONFIG_USB_STORAGE_DATAFAB is not set
# CONFIG_USB_STORAGE_FREECOM is not set
# CONFIG_USB_STORAGE_ISD200 is not set
# CONFIG_USB_STORAGE_USBAT is not set
# CONFIG_USB_STORAGE_SDDR09 is not set
# CONFIG_USB_STORAGE_SDDR55 is not set
# CONFIG_USB_STORAGE_JUMPSHOT is not set
# CONFIG_USB_STORAGE_ALAUDA is not set
# CONFIG_USB_STORAGE_ONETOUCH is not set
# CONFIG_USB_STORAGE_KARMA is not set
# CONFIG_USB_STORAGE_CYPRESS_ATACB is not set
# CONFIG_USB_STORAGE_ENE_UB6250 is not set
CONFIG_USB_UAS=m
# CONFIG_USB_LIBUSUAL is not set

                                                                                  
                                                                                                                           