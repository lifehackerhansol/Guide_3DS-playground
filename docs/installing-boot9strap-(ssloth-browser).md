# Installing boot9strap (SSLoth-Browser)

::: details Technical Details (optional)

In order to exploit the Browser application, we need to bypass the browser version check, which is designed to disallow the use of the browser without updating to the latest system version.

A public proxy server is available, which, with the help of the SSLoth exploit, can bypass this check.

Once the bypass is active, an exploit webpage will be accessible which will do the rest of the job.

For technical details on the exploits that you will be using on this page, see [here](https://github.com/MrNbaYoh/3ds-ssloth) (SSLoth) and [here](https://github.com/TuxSH/universal-otherapp) (universal-otherapp).

:::

## Compatibility Notes

SSLoth allows users on version 11.13.0 and below to bypass the browser version check, allowing the use of new-browserhax or old-browserhax (compatible with versions 11.4.0 through 11.13.0 in all regions), which can then be used in conjunction with universal-otherapp.

## What You Need

* The latest release of [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/download/v0.0.7/SafeB9SInstaller-20170605-122940.zip) (direct download)
* The latest release of [boot9strap](https://github.com/SciresM/boot9strap/releases/download/1.4/boot9strap-1.4.zip) (direct download)
* The latest release of [Luma3DS](https://github.com/LumaTeam/Luma3DS/releases/latest) (the Luma3DS `.zip` file)
* The latest release of [universal-otherapp](https://github.com/TuxSH/universal-otherapp/releases/latest) (`otherapp.bin`)

## Instructions

### Section I - Prep Work

In this section, you will copy the files needed to trigger both browserhax and universal-otherapp.

1. Power off your console
1. Insert your SD card into your computer
1. Copy `otherapp.bin` to the root of your SD card and rename it to `arm11code.bin`
    + The root of the SD card refers to the initial directory on your SD card where you can see the Nintendo 3DS folder, but are not inside of it
    + If you do not see the `.bin` extension, do not add it to the end of the filename
1. Copy everything from the Luma3DS `.zip` to the root of your SD card
1. Create a folder named `boot9strap` on the root of your SD card
1. Copy `boot9strap.firm` and `boot9strap.firm.sha` from the boot9strap `.zip` to the `/boot9strap/` folder on your SD card
1. Copy `SafeB9SInstaller.bin` from the SafeB9SInstaller `.zip` to the root of your SD card
1. Reinsert your SD card into your console
1. Power on your console

### Section II - SSLoth

In this section, you will change your Internet connection settings to use a proxy network designed to bypass the browser version check, allowing the browser to function without a system update. This will allow you to access the browser exploit webpage in the next section.

<!--@include: ./_include/addproxy.md -->
1. Press "Back" twice, then "Close" to go back to the HOME Menu

### Section III - Launching SafeB9SInstaller

In this section, you will visit the browser exploit webpage, which will use universal-otherapp to launch the boot9strap (custom firmware) installer.

1. On the HOME Menu, press the Left and Right shoulder buttons at the same time to open the camera
    + If you are unable to open the camera, open the Internet Browser and manually type the URL instead (`https://zoogie.github.io/web/nbhax/`)
1. Tap the QR code button and scan [this QR code](http://api.qrserver.com/v1/create-qr-code/?color=000000&bgcolor=FFFFFF&data=https%3A%2F%2Fzoogie.github.io%2Fweb%2Fnbhax&qzone=1&margin=0&size=400x400&ecc=L)
    + If you get a crash or an error code, [follow this troubleshooting guide](troubleshooting-ssloth-browser)
    + If you get a security certificate warning, press (A) to allow the connection
1. Tap the "PROCEED TO HAXX" button
1. If the exploit was successful, you will have booted into SafeB9SInstaller
    + If you get an error, [follow this troubleshooting guide](troubleshooting-ssloth-browser)

### Section IV - Installing boot9strap

In this section, you will install custom firmware onto your console.

1. When prompted, input the key combo given on the top screen to install boot9strap
    + If a step on the lower screen has red-colored text, and you are not prompted to input a key combo, [follow this troubleshooting guide](troubleshooting-ssloth-browser)
1. Once it is complete, press (A) to reboot your console
<!--@include: ./_include/configure-luma3ds.md -->

### Section V - Restoring default proxy

<!--@include: ./_include/rmproxy.md -->

<!--@include: ./_include/luma3ds-installed-note.md -->
___

::: tip

Continue to [Finalizing Setup](finalizing-setup)

:::
