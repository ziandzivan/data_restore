> **Warning** Work in progress

# data_restore

## Introduction
Script of restoring User Data backup (created by ![data_backup.sh](https://github.com/ziandzivan/data_backup)) or from booted system with Magisk or from TWRP.

### ***Screenshots***

<img width="300" height="600" src="https://raw.githubusercontent.com/ziandzivan/data_restore/main/assets/Screenshot_20230301-132028.png"> <img width="300" height="600" src="https://raw.githubusercontent.com/ziandzivan/data_restore/main/assets/Screenshot_2023-03-02-03-36-34.png">

## Supported devices  
  
### ***First-grade support***
  
on my hands:
- Google Pixels
- HTC
  
### ***Others***

- Asus Rog Phone
  
some:
- Xiaomi, POCO

## Requirement

- or Magisk 20.4+ Android 9+ for restoring from booted system
- or Android 7+ for restoring from TWRP.

## Installing script

A latest script `data_restore_v2.xx-MAGISK-TWRP.zip` will be copied to the root of Internal storage by installing a Magisk module `data_restore_Courier_v2.xx-MAGISK.zip`. data_restore_Courier module ONLY delivers the latest version of the script to intSD.
- Download the module and copy it to internal storage.
- In the Magisk App: Modules - Install from storage - select the downloaded `data_restore_Courier module` - Reboot. 
- Find the `data_restore_v2.xx-MAGISK-TWRP.zip` script in the root of intSD. Done, now you can use this script.

## Running script

There are 2 variants for running `data_restore_v2.xx-MAGISK-TWRP.zip` script:
1. From `booted system`, running from Magisk module installer.
2. Also from `TWRP` if it is avaialble for a device. 

## Features of restoring data

- Check or put to the root of any storage device a folder `databackup` with all files and archive `data*.tar` created at backuping.
- First the script is looking for `databackup` on mounted USB-OTG, then on extSD and after on intSD. Unmount or extract external storage devices if you need restoring backup from internal SD.
- The script automatically recognizes Multy-volume backup.
- Open `databackup.log` and look at backuping parameters. Restoring is possible ONLY on the same system build number or higher. Also the same Magisk version is required for correct restoring.
- Before restoring there is no necessity to remove your fingerprint, screen lock pattern, pin or password. In case restoring is without format of data partition, current before restoring sets of screen lock will be saved and not changed after restoring. In another case they will be removed.

### ***From system*** (HTC Android 9, Google Pixels Android 11+, Asus Rog Android 10+)
- Restoring is possible from working system with root, Magisk 20.4+. Running `data_restore_v2.xx-MAGISK-TWRP.zip` is from Magisk module installer. 
- After confirming restoring by Volune Up batton 
