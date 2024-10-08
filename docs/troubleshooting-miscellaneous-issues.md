# Troubleshooting miscellaneous issues on consoles with custom firmware

This page offers troubleshooting advice for commonly encountered issues on a console with custom firmware. If you are unable to solve your issue with the advice on this page, please join [Nintendo Homebrew on Discord](https://discord.gg/MWxPgEp) and describe your issue, including what you have already tried.

## Other troubleshooting

::: details Clear HOME Menu extdata

1. Power off your console
1. Insert your SD card into your computer
1. Navigate to the `/Nintendo 3DS/<ID0>/<ID1>/extdata/00000000/` folder on your SD card
1. Delete the corresponding folder for your 3DS region:
    + **EUR Region**: `00000098`
    + **JPN Region**: `00000082`
    + **USA Region**: `0000008f`
    + **CHN Region**: `000000A1`
    + **KOR Region**: `000000A9`
    + **TWN Region**: `000000B1`
1. Reinsert your SD card into your console

:::

::: details Clear HOME Menu theme data

1. Power off your console
1. Insert your SD card into your computer
1. Navigate to the `/Nintendo 3DS/<ID0>/<ID1>/extdata/00000000/` folder on your SD card
1. Delete the corresponding folder for your 3DS region:
    + **EUR Region**: `000002ce`
    + **JPN Region**: `000002cc`
    + **USA Region**: `000002cd`
    + **KOR Region**: `000002cf`
1. Reinsert your SD card into your console

:::

::: details Manually entering Homebrew Launcher

If you are missing the Homebrew Launcher application from your HOME Menu, you can follow these instructions to manually enter the Homebrew Launcher. (You will need [boot.3dsx and boot.firm](https://github.com/LumaTeam/Luma3DS/releases/latest) on the root of your SD card.)

<!--@include: ./_include/launch-hbl-dlp.md -->

:::

::: details Turning off Parental Controls

You can disable the Parental Controls feature by going to System Settings -> Parental Controls and inserting the PIN, then pressing "Clear Settings", then "Delete" to remove it.
However, if you do not know the PIN and therefore cannot access the console's settings, you will need to disable it. In order to do this, you need to obtain your console's master key (mkey):
1. Go to [this website](https://mkey.eiphax.tech/)
1. Fill the following boxes with the information:
    + Device Type: Select "3DS" (the same applies if you are using a 2DS, New 3DS (XL/LL) or New 2DS (XL/LL))
    + System Date: The day and month your console's clock is set to
    + Inquiry Number: Can be obtained by pressing "Forgot PIN" then "I Forgot" in the Parental Controls screen
1. After you have obtained your mkey, press OK on the screen you have obtained your Inquiry Number, then input the master key
1. Press "Clear Settings", then "Delete" to remove all Parental Controls data

:::

<!--@include: ./_include/troubleshooting-footer.md -->
