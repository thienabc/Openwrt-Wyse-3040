# Openwrt-Wyse-3040
Step 1:  Preparing term:
Download any fw: https://downloads.openwrt.org/. 
Mayble, https://downloads.openwrt.org/releases/23.05.4/targets/x86/64/

Eg: openwrt-23.05.4-x86-64-generic-squashfs-combined-efi.img.gz. 
Extract: openwrt-23.05.4-x86-64-generic-squashfs-combined-efi.img 
=>>> Copy to USB (no need USB boot) 
+ USB 1 contain FW openwrt
+ USB2 is USB boot
+ Linux iso: MX-23.3 64 bit (or any live linux)

Step 2: USB boot
Create USB boot by ventoy-1.0.99. That is the best solution for USB boot iso. 

Step 3: Can use any Linux iso
Here, download MX-23.3 64 bit
https://mxlinux.org/torrent-files/ 
copy file: MX-23.3 64 bit into USB boot at step 2 (meaning USB 2)

step 4: Power on Wyse 3040 and press F12 to menu boot / choose USB boot at step 2

Step5: Clone partition from ISO
+ go to USB1 / right click mouse empty blank with menu command: Open Terminal here.
+ if linux ask and have announce show pass: demo (password is demo)
+ code clone partition: dd if=xxx.img bs=1M of=/dev/mmcblk0  (xxx: is a filename of Step 1)
+ Specific code: dd if=openwrt-23.05.4-x86-64-generic-squashfs-combined-efi.img bs=1M of=/dev/mmcblk0

