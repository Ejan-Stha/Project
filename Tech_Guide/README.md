# How to create muti bootable USB from Mac?

-	Requires minimum 32 GB or more USB
  
-	Format the USB (recommended MS-DOS (FAT32))
  
-	Download balenEthcher and Ventoy iso
  
*File name:* ventoy-1.1.05-livecd.iso

*Ventoy:* https://www.ventoy.net/en/download.html

*BalenEthcer:* https://etcher.balena.io/

-	Insert USB and open balenEthcher
 
-	Select target as USB and upload the ventoy.iso file

  
  ![Open_BalenaEthcer](Images/Open_BalenaEthcer.png)


-	Press Flash
  
  ![Flash](Images/Flash.png)

 
-	Successful Flash
 
   ![Flash_completed](Images/Flash_completed.png)


-	Boot into the device

   ![Boot_Ventoy](Images/Boot_Ventoy.jpg)


-	Press install.
 
  ![Install_Package](Images/Install_Package.jpg)
  

  ![Succefully_installed](Images/Succefully_installed.jpg)
 

-	After successful install press cross
  
 
  ![Close_Ventoy](Images/Close_Ventoy.jpg)

  

  ![no_ISO](Images/no_ISO.jpg)



-	Drag and drop multiple ISO file such as PeppermintOS, Ubuntu, ShredOS etc and boot it into the system.

  ![Successfully_installed_ISO](Images/Successfully_installed_ISO.jpg)

 
-	Test and check
-	End

---
  
**Note:** Do not flash another ISO file after flashing Ventoy.iso file from balenEthcher. After flashing ventoy.iso file, the drive Is unreadable, and we cannot copy other ISO file into the drive. For this, we need to boot the ventoy,iso into the system and install, after installation, we can remove the drive and it will be readable and we can easily drag and drop ISO file inside the drive.

---
