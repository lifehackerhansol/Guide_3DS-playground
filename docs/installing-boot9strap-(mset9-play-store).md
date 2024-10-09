# Installing boot9strap (MSET9 Play Store)

::: details Technical Details (optional)

[MSET9](https://github.com/zoogie/MSET9) is an exploit for the System Settings application developed by [zoogie](https://github.com/zoogie). It exploits a flaw where the ID1 (the second 32-character folder name inside of the Nintendo 3DS folder, inside of the ID0) can be *any* name as long as it is 32 characters. Performing a specific sequence of actions results in the console executing the instructions that are encoded into the ID1 folder name, which can be used to grant full control over the 3DS.

:::

## Compatibility Notes

::: warning

This page requires an Android phone/tablet or a Chromebook. If you have a computer running Windows, macOS, or Linux, follow [Installing boot9strap (MSET9 CLI)](installing-boot9strap-(mset9-cli)) instead. If you do not have access to any of these devices, you will need to use an [alternate exploit](https://wiki.hacks.guide/wiki/3DS:Alternate_Exploits).

:::

::: warning

On Android phones/tablets, the minimum Android version required is 6.0 (Marshmallow).

:::

## What You Need

* The following applications installed from the Google Play Store:
    * [MSET9 Installer](https://play.google.com/store/apps/details?id=moe.saru.homebrew.console3ds.mset9_installer_android)
    * [ZArchiver](https://play.google.com/store/apps/details?id=ru.zdevs.zarchiver)
    * If you wish, you can sideload these applications instead
* The latest release of [MSET9](https://github.com/zoogie/MSET9/releases/latest) (the Release `.zip` file)

## Instructions

### Section I - Prep Work

In this section, you will prepare the SD card data necessary for the MSET9 exploit to trigger.

1. Power on your console **with your SD card inserted**
1. Open Mii Maker
1. Wait for your console to reach the "Welcome to Mii Maker" screen, then exit Mii Maker
    + You may see [this screen](/images/screenshots/mset9/mii-extdata.png), which indicates the necessary data has been created
    + If you just reach the normal Mii Maker screen, exit Mii Maker and continue to the next step
1. Power off your console
1. Insert your SD card into your phone/tablet/computer
1. Copy everything from the Release `.zip` to the root of your SD card, overwriting any existing files:
    + Open ZArchiver
    + If prompted, [allow ZArchiver to access files on your SD card](/images/screenshots/mset9/zarchiver-allow.png)
    + Navigate to where the downloaded MSET9 Release `.zip` is located ([likely in the Downloads folder](/images/screenshots/mset9/zarchiver-zip-location.png))
    + Select the Release `.zip`, then select "Extract..." ([image](/images/screenshots/mset9/zarchiver-extract-1.png))
    + Navigate to your SD card, then tap the blue 'down arrow' icon to extract the files to the root of your SD card ([image](/images/screenshots/mset9/zarchiver-extract-2.png))

    ::: info

    ![](/images/screenshots/mset9/mset9-root-layout-android.png)

    :::

1. Run the [MSET9 Installer application](/images/screenshots/mset9/mset9-setup-android.png)
1. Tap on `Select "Nintendo 3DS" Folder`, then navigate to your `Nintendo 3DS` folder on your SD card ([image](/images/screenshots/mset9/select-mset9-folder-1.png))
1. Once inside the `Nintendo 3DS` folder, tap on "Use this folder", then "Allow" if asked ([image](/images/screenshots/mset9/select-mset9-folder-2.png))
1. If "Setup MSET9" is [highlighted](/images/screenshots/mset9/setup-mset9-highlighted.png), proceed to the next step. **Do not setup MSET9 yet.** Close the MSET9 Installer for now
    + If "Check Again" is highlighted, there is a problem that you need to resolve before you can use MSET9. Refer to the [troubleshooting](troubleshooting-mset9)
1. Reinsert your SD card into your console
1. Power on your console

### Section II - MSET9

In this section, you will trigger MSET9 to launch SafeB9SInstaller (the custom firmware installer).

::: danger

These instructions must be followed **EXACTLY**, so double-check EVERYTHING you are doing to avoid errors!

:::

1. **[Hover over](/images/screenshots/mset9/hover-settings.png)** the System Settings icon using the D-Pad (do not select it yet)
1. Power off, then power on your console
1. Press (A) to launch System Settings
1. Navigate to `Data Management` -> `Nintendo 3DS` -> `Extra Data` ([image](/images/screenshots/mset9/settings-extdata.png))
1. **Do not press any buttons or touch the screen**
1. **With the console STILL ON, and without pressing any buttons or touching the screen**, remove your SD card from your console
    + The menu will refresh and say that no SD card is inserted, which is expected
1. Insert your SD card into your phone/tablet/computer
1. Open the MSET9 Installer application
1. Tap "Setup MSET9"
1. Tap on the photo corresponding to your console model, then on the button corresponding to your current firmware version
    + If the injection was successful, all buttons should become grayed out except for "Remove MSET9"
1. Reinsert your SD card into your console **without pressing any buttons or touching the screen**
1. If the exploit was successful, you will have booted into SafeB9SInstaller 
    + If you get a red screen or the console gets stuck on a loading screen, follow the [troubleshooting guide](troubleshooting-mset9)

### Section III - Installing boot9strap

In this section, you will install custom firmware onto your console.

1. When prompted, input the key combo given on the top screen to install boot9strap
    + If a step on the lower screen has red-colored text, and you are not prompted to input a key combo, [follow this troubleshooting guide](troubleshooting-mset9)
1. Once it is complete, press (A) to reboot your console
<!--@include: ./_include/configure-luma3ds.md -->

### Section IV - Removing MSET9

In this section, you will remove MSET9 to prevent further issues. (This will not remove the custom firmware that you just installed.)

::: danger

Do NOT skip this section! If you skip it, applications may crash unexpectedly and you will encounter errors on the next page!

:::

1. Power off your console
1. Insert your SD card into your phone/tablet/computer
1. Open the MSET9 Installer application
1. Tap "Remove MSET9"
1. Close the MSET9 Installer application

<!--@include: ./_include/luma3ds-installed-note.md -->

___

::: danger

Did you follow Section IV (Removing MSET9)? That section is MANDATORY!

:::

::: tip

Continue to [Finalizing Setup](finalizing-setup)

:::
