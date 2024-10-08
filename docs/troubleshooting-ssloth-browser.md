# Troubleshooting (SSLoth-Browser)

This page offers troubleshooting advice for commonly encountered issues with the "Installing boot9strap (SSLoth-Browser)" page. If you are unable to solve your issue with the advice on this page, please join [Nintendo Homebrew on Discord](https://discord.gg/MWxPgEp) and describe your issue, including what you have already tried.

## Issues with SSLoth-Browser

::: details Red/purple/pink and white screen after running Browserhax

This likely indicates that you already have custom firmware. You should [check for CFW](checking-for-cfw).

:::

::: details "An error has occurred. Hold down the POWER button to turn off the power..." (black screen with text)

The file `arm11code.bin` is missing or misplaced. Download the latest release of [universal-otherapp](https://github.com/TuxSH/universal-otherapp/releases/latest), place `otherapp.bin` on the root of your SD card and rename it to `arm11code.bin`. Do not add the `.bin` extension if you do not already see it.

:::

::: details "An error has occurred, forcing the software to close..." (white message box)

There may be an issue with your `arm11code.bin` file. Download the latest release of [universal-otherapp](https://github.com/TuxSH/universal-otherapp/releases/latest), place `otherapp.bin` on the root of your SD card and rename it to `arm11code.bin`. Do not add the `.bin` extension if you do not already see it.

You can also try resetting your browser save data:

1. Launch the browser, then launch the browser settings
1. Scroll to the bottom and select "Reset Save Data" (it may also be called "Initialize Save Data" or "Clear All Save Data")
1. Try the exploit again

:::

::: details Opening the browserhax QR code or URL crashes

Browser based exploits (such as this one) are often unstable and crash frequently, but they can sometimes be fixed by doing the following steps.

1. Launch the browser, then launch the browser settings
1. Scroll to the bottom and select "Reset Save Data" (it may also be called "Initialize Save Data" or "Clear All Save Data")
1. Try the exploit again

:::

::: details System Update prompt when opening browser

The SSLoth proxy was incorrectly configured. Re-do the SSLoth section on the page.

:::

::: details Error 032-0420 when opening browser

Follow these steps in order:

1. Launch System Settings on your console
1. Navigate to `Internet Settings` -> `Connection Settings`
1. Click on your network connection slot and navigate to `Change Settings` -> `Next Page (right arrow)` -> `Proxy Settings`
1. Set "Proxy Settings" to "No"
1. Click OK, then click Save
1. When prompted, click "Test" to perform the connection test
    + The test should succeed
1. Click "OK" to continue
1. Press "Back" twice, then "Close" to go back to the HOME Menu
1. Open the Internet Browser once
1. If prompted about a system update, press OK
    + This won't actually update the system
1. Start again from [Section II](installing-boot9strap-(ssloth-browser).html#section-ii---ssloth)

:::

::: details Frozen on "Doing agbhax..."

There may be an issue with your `arm11code.bin` file. Re-download the latest release of [universal-otherapp](https://github.com/TuxSH/universal-otherapp/releases/latest), place it on the root of your SD card, and rename it to `arm11code.bin`. Do not add the `.bin` extension if you do not already see it.

:::

::: details "PrepareArm9ForTwl returned error c8804631!"

Join [Nintendo Homebrew on Discord](https://discord.gg/MWxPgEp) for assistance.

:::

::: details Failed to mount the SD card!

Back up your data and reformat your SD card as FAT32 with the recommended tool depending on your operating system ([Windows](formatting-sd-(windows)), [macOS](formatting-sd-(mac)), [Linux](formatting-sd-(linux))). MiniTool Partition Wizard and the HP formatting tool (HPUSBDisk) are known to cause issues with 3DS SD cards.

If this is unsuccessful, try using another SD card.

:::

<!--@include: ./_include/troubleshooting-sb9si-common.md -->

<!--@include: ./_include/troubleshooting-footer.md -->
