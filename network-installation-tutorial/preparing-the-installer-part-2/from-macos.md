---
description: Installing Clover by using the installer package.
---

# From macOS

## Part - 1

1. Open Terminal and run `pkgutil --expand [drag and drop the RecoveryHDMetaDmg.pkg in gibMacOS/macOS Downloads/publicrelease/xxx-xxxxx xx.xx.x macOS xxxx folder] Desktop/RecoveryFiles`By doing the above command, it will extract files from the recovery package and create a folder call RecoverFiles on desktop to save all extracted resources. 
2. Go inside the RecoverFiles folder, double click on RecoveryHDMetaDmg.dmg and the disk image should be mounted.
3. Go into the RecoveryHDMeta disk and copy BaseSystem.dmg to desktop.
4. Go to disk utility. Find your USB and format it to:  `Name: [whatever you want] Format: Mac OS Extended (Journaled)  Scheme: GUID Partition Map`
5. Now click Restore button in Disk Utility and choose Image...
6. Choose BaseSystem.dmg on desktop and press Restore.
7. This should take some time depending on your USB speed.

![Steps 1 - 3 \(Extracting the resources\)](../../.gitbook/assets/extract-resources-files.gif)

![Steps 4 - 7 \(Restoring the resources to USB\)](../../.gitbook/assets/restoring-to-usb.gif)

## Part - 2

1. Open the Clover installer
2. Install it to your USB with these settings \(choose Customize in the Installation Type\) `Clover for UEFI booting only Install Clover in the ESP UEFI Drivers:  - ApfsDriverLoader  - AptioMemoryFix  - HFSPlus (or VBoxHFS - 64) Install RC Scripts on target volume (or Install RC Scripts on other volumes)` More explanations [here](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/clover-setup).
3. When it is finished, a disk call EFI should be mounted. Replace the original config.plist in EFI/EFI/CLOVER with the downloaded sample config \(**or the pre-patched one for AMD Users** which mentioned [here](../get-started/untitled/amd-clover-config.plist.md)\).
4. After that, put all kexts you have downloaded \(in [Gathering Kexts page](../get-started/untitled/gathering-kexts.md)\) to `EFI/EFI/CLOVER/kexts/Other` folder.
5. You have finally made the installer! Woo-hoo! 🥳 

![Steps 1 - 2 \(Installing Clover\)](../../.gitbook/assets/installing-clover.gif)

![Step 3](../../.gitbook/assets/copying-config.gif)

