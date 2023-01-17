---
title: Configuring a Proxmox Cluster
date: 2023-12-28 12:00:00
categories: [Servers]
tags: [Dell,Servers,Raid]
---
# Flash Dell R720 into IT Mode

Download the firmware for your RAID card from the Dell website. Be sure to download the IT firmware version. Make sure that you are downloading the firmware for the specific RAID card model that is installed in your R720.

Create a bootable USB drive with the firmware. You can use a tool like Rufus for this. Rufus is a free and open-source tool that can be used to create a bootable USB drive from an ISO file.
 
Connect the USB drive to the server and power it on.
Press F11 during the boot process to enter the boot menu. This will bring up the One-time Boot Menu.

Select the USB drive as the boot device. You will have to use the arrow keys to select the USB drive and then press Enter.

Once the firmware update utility has loaded, select the firmware file you downloaded earlier and begin the flashing process. Follow the on-screen instructions to complete the flashing process.

Once the flashing process is complete, the server will reboot. It's important to note that you should not interrupt the flashing process as it may damage the RAID card.

After the server has rebooted, check the RAID card's firmware version to confirm that it has been successfully updated to IT mode. You can check the firmware version using the RAID card's BIOS or by using the RAID card's management software.

Configure the Operating system to recognize the RAID card as a standard HBA and use the operating system's native software RAID or ZFS or any other RAID software.

It is important to note that flashing the firmware to IT mode will erase all data from the RAID card and will require you to reconfigure the RAID or HBA settings after flashing. Therefore, it is extremely important to have a backup of your data before starting this process and to have a good understanding of how to configure the Operating system to work with the HBA.

It is also a good idea to test the RAID card in a lab environment before deploying it to a production environment. This will allow you to verify that the RAID card is working as expected and that you have configured the Operating system correctly.