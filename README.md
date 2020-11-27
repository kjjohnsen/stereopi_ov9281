# stereopi_ov9281
Source code for supporting two ov9281 on the stereopi1

To install, use the device-tree-compiler to build each file.  
- dt-blob.dts goes to dt-blob.bin in /boot
- The other two go to /boot/overlays (make sure the names match with the overlays in config.txt)
- Take the relevant lines from config.txt and put in your /boot/config.txt

These are based on the stereopi dt-blob.dts found on their wiki, and the source in the 5.4 rpi Linux kernel. 
