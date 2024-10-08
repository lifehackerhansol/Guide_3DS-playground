# Troubleshooting (Soundhax)

This page offers troubleshooting advice for commonly encountered issues with the "Installing boot9strap (Soundhax)" page. If you are unable to solve your issue with the advice on this page, please join [Nintendo Homebrew on Discord](https://discord.gg/MWxPgEp) and describe your issue, including what you have already tried.

## Issues with Soundhax

::: details Red/purple/pink and white screen after running Soundhax

If your console is on system version 9.4.0, 9.5.0, or 9.6.0, you may be encountering a bug with an old version of universal-otherapp. Download the latest version from [here](https://github.com/TuxSH/universal-otherapp/releases/latest).

If your console is not on those firmwares, it likely indicates that you already have custom firmware. You should [check for CFW](checking-for-cfw).

:::

::: details "An error has occurred, forcing the software to close..." (white message box)

There is an issue with your `otherapp.bin` file (it is missing, misplaced, or corrupted). Download the latest release of [universal-otherapp](https://github.com/TuxSH/universal-otherapp/releases/latest) and place it on the root of your SD card.

:::

::: details "Could not play"

You have the wrong Soundhax file for your console and region, or your console is incompatible with Soundhax. In the latter case, your course of action will determine on what version your 3DS is currently on. Join [Nintendo Homebrew on Discord](https://discord.gg/MWxPgEp) for assistance.

:::

::: details Failed to mount the SD card!
Back up your data and reformat your SD card as FAT32 with the recommended tool depending on your operating system ([Windows](formatting-sd-(windows)), [macOS](formatting-sd-(mac)), [Linux](formatting-sd-(linux))). MiniTool Partition Wizard and the HP formatting tool (HPUSBDisk) are known to cause issues with 3DS SD cards.

If this is unsuccessful, try using another SD card.

:::

<!--@include: ./_include/troubleshooting-sb9si-common.md -->

<!--@include: ./_include/troubleshooting-footer.md -->
