# Asus Zephyrus M (GM501GS) macOS Mojave 10.4.4

Specs:\
OS: Mac OS High Sierra 10.14.4\
CPU i7 8750H Code Lake\
Chipset: HM370\
Graphics: Intel UHD 630 (has NVIDIA 1070 TI, but not supported by 10.14, so have DSDT to disable it.)\
Wi-Fi: Dell DW1830\
Bluetooth:\
Camera: USB2.0 HD UVC WebCam\
Audio/Mic: Realtek HD Audio ALC3328 (ALC294 codec)\
Keyboard & Trackpad - ELAN/SA473I-12A4 (ELAN1201)

### Installing  

Use olaria bootup https://www.olarila.com/forum/viewtopic.php?f=51&t=6743  
Use clover with default settings and install to Macintosh HD https://sourceforge.net/projects/cloverefiboot/  
restart and unplug usb and boot from new uefi clover and sewlect macintosh hd  
add lilu and whatever green kexts.


## What worked OTB

Wi-Fi\
Intel Graphics I believe, may need to do some frame buffering, but will test.\
Keyboard

## What I had to fix
Bluetooth, fixed with BrcmFirmwareRepo.kext and BcrmPatchRam2.kext, not sure if original bluetooth works  
Native Brightness Controler, used AppleBacklightFixup.kext with SSDT-PNLF.aml in patched folder
Issues with lag when asking for admin password, used NoTouchID.kext\
Battery manager, fixed with ACPIBatteryManager.kext\
Audio, fixed with AppleALC.kext and changing Audio Inject to 13 in clover config.plist\
FNKeys, used Karabiner to alter  

### What doesn't work

Trackpad\
Keyboard backlight control  

## Helpful links.

https://www.insanelymac.com/  
https://www.reddit.com/r/hackintosh/  
https://www.olarila.com/  
https://www.tonymacx86.com/  


## Acknowledgments  

*Special thanks to dggomes. I used his High Sierra build to first install and then wanted to install Mojave.  
*You can find his build for High Sierra here: https://github.com/dggomes/asuszephyrus-m  
