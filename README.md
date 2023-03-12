> **Warning** Work in progress

# data_restore

## Introduction
Script of restoring User Data backup (created by ![data_backup.sh](https://github.com/Magisk-Modules-Alt-Repo/data_backup)) or from booted system with Magisk or from TWRP.

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

## Installing and Updating

The latest script `data_restore_v2.xx-MAGISK-TWRP.zip` will be copied to the root of Internal storage by installing a ![Magisk Courier-module](https://github.com/ziandzivan/data_restore_Courier) `data_restore_Courier_v2.xx-MAGISK.zip`. The data_restore_Courier module ONLY delivers the latest version of the script to intSD (![README](https://github.com/ziandzivan/data_restore_Courier#readme)).

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
- After confirming restoring by Volune Up batton, the screen will be switched off and restoring will be started.
- > **Warning** _Do not touch the device, wait for finishing restoring and automatic rebooting to system !_ 
- Restoring log is written to `datarestore.log` file in `databackup` folder. Through the PC you can spy on the progress of execution, the file will be replenished.

### ***From TWRP*** (if exist for the device)
- For Google Pixels Android 11+, Asus Rog Android 10+ any wipes in TWRP are not required! Restoring from TWRP should be started on the existing configured system.
- Choose a workable variant. For example, restoring data backup on HTC Android 7+ is possible only after format of data partition in TWRP. After format reboot TWRP and run `data_restore_v2.xx-MAGISK-TWRP.zip` script.

## Parameters

The script can be launched with keys. They should be written in the name of the script file, for example: `data_restore_v2.xx-MAGISK-TWRP-m.zip`

***#1***

`-m` - restoring of the backup with the exception of ***media***, i.e. without restoring of all contents of the internal storage in the backup;

***#2***

`-r` - restoring with the exception of ***root*** Magisk files, i.e. similarly as removal at Magisk uninstaller. It is useful in some cases, for example, for the subsequent installation of a new version of Magisk. Similarly as well as at uninstall of Magisk in TWRP, and in this case will be removed all root files except the base manager Magisk application which if necessary can be removed from the system as like any other application. Restoring of screen adjustments values at rebooting will take place as soon as will be installed root.
> NOTE: _Do not hurry and not install there and then the root in TWRP.  First be once booted in the system with restored data without the root, then install it !_

***#3***

`-a` - despite of presence of any keys above, always to ***ask*** establishing these restoring modes manually with a dialogue Yes/No.

## First booting to system

- After first booting to system with the root will be the rebooting during a few minutes. With second booting will be restoring of screen adjustments values.
- If the root was removed, switch off Air plane mode and set preferable screen adjustments values. After installing the root back it will be restored automatically.
- After restoring from TWRP with a preliminary format data, renominate fingerprint and screen lock pin, password or graphic key.
