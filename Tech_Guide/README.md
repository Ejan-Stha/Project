How to create muti bootable USB from Mac?
-	Requires minimum 32 GB or more USB
-	Format the USB (recommended MS-DOS (FAT32))
-	Download balenEthcher and Ventoy iso
File name: ventoy-1.1.05-livecd.iso
Ventoy: https://www.ventoy.net/en/download.html
BalenEthcer: https://etcher.balena.io/
-	Insert USB and open balenEthcher
 
-	Select target as USB and upload the ventoy.iso file 
  ![Network_diagram](Screenshot/Network_diagram.png)




-	Press Flash
  
 
-	Successful Flash
 
 

-	Boot into the device
 

-	Press install.
 

 

-	After successful install press cross
 

 

-	Drag and drop multiple ISO file such as PeppermintOS, Ubuntu, ShredOS etc and boot it into the system.


 

-	Test and check
-	End
Note: Do not flash another ISO file after flashing Ventoy.iso file from balenEthcher. After flashing ventoy.iso file, the drive Is unreadable, and we cannot copy other ISO file into the drive. For this, we need to boot the ventoy,iso into the system and install, after installation, we can remove the drive and it will be readable and we can easily drag and drop ISO file inside the drive.

