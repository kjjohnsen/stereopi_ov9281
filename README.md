# stereopi_ov9281
Source code for supporting two ov9281 (inno-maker.com) on the stereopi1 (Requires Kernel 5.4+ with built-in ov9281 driver, and compute module 3, though it should be possible to modify for cm1).

Basically, how this works is to use a software-based i2c for pins 0 and 1 instead of tying them to the hardware i2c.  This lets you use two i2c-address-locked ov9281 cameras (from inno-maker.com). 

To install, use the device-tree-compiler to build each file.  
- dt-blob.dts goes to dt-blob.bin in /boot
- The other two go to /boot/overlays (make sure the names match with the overlays in config.txt)
- Take the relevant lines from config.txt and put in your /boot/config.txt

These are based on the stereopi dt-blob.dts found on their wiki, and the source in the 5.4 rpi Linux kernel. 
