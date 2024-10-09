# FAQ

::: danger

<!--@include: ./_include/3ds-online.md -->

:::

::: info

**Yes**, you can still install custom firmware on your 3DS, even after the closure of eShop.

:::

## Pre-Installation FAQ

::: details I am on the latest system version. Is my console hackable without any external hardware/prerequisites?

**Yes!** New 3DS / New 3DS XL / New 2DS XL can use [super-skaterhax](installing-boot9strap-(super-skaterhax)), while 3DS / 3DS XL / 2DS can use [MSET9](installing-boot9strap-(mset9)).

:::

::: details What consoles is this guide compatible with?

This guide is compatible with all retail 3DS-family devices (3DS, 3DS XL, 2DS, New 3DS, New 3DS XL, New 2DS XL). If your system version string is displayed as "0.0.0-0", then you may have a developer unit.

:::

::: details How risky is hacking my console?

Bricks are now effectively impossible unless you are purposely trying to brick your console.

:::

::: details Can I run awesome homebrew and emulators with this?

Yes! This guide will install a few useful homebrew applications, including [Universal-Updater](https://github.com/Universal-Team/Universal-Updater/releases/latest), which acts as a homebrew app store.

:::

::: details Can I use this to play games from other regions?

Yes; Luma3DS will automatically ignore the region check for cartridges and installed titles. Some games may need to make use of Luma's [locale emulation feature](https://wiki.hacks.guide/wiki/3DS:Setting_game_locales) in order to work properly on out-of-region consoles.

:::

::: details Will I lose any features if I install CFW?

No. Consoles with custom firmware can download game updates and run physical cartridges as any other 3DS can.

:::

::: details Can I keep my NNID, saves, digital games (etc.)?

Your NNID (if you have one) will not be affected by this guide. Consoles with a region of KOR, CHN, or TWN do not have NNID functionality to begin with and are thus unaffected.

Following this guide alone should not result in data loss (saves, digital games, etc), but SD card corruption is always a possibility. You should make a backup of your SD card contents if you have important data.

:::

::: details Will my 3DS be banned for having CFW?

Bans are no longer possible because Nintendo Network services have been shut down (for everyone).

:::

::: details Can I do this without a computer (e.g. an Android phone)?

Yes! All you need is the ability to put files on a compatible SD card.

:::

::: details What size SD card can I use?

You will need at least 1.5GB of free SD card space to follow this guide in its entirety. While the 3DS is officially compatible with SD cards up to 32GB, larger SD cards can be used if they are manually re-formatted as FAT32. It is not recommended to use SD cards greater than 128GB due to known issues with GBA graphics and custom themes.

:::

::: details I heard about this thing I have to pay for (Gateway, Sky3DS, ntrboot, R4, etc). Is that something I need?

No. While a DS flashcart can be used to mod a 3DS using [ntrboot](ntrboot), there is now a free software method available for most consoles.

3DS-mode flashcarts like Gateway and Sky3DS are not recommended because they are obsolete and may carry brick risk.

:::

::: details What's the difference between custom firmware and homebrew?

Definitionally speaking, custom firmware refers to a modification of the 3DS system software to do things that it normally isn't able to. Homebrew generally refers to software created outside of official sources (i.e. not distributed by eShop or cartridges).

Historically, the 3DS used to have userland homebrew access through older exploits like ninjhax, which people sometimes called just "homebrew". The level of system access granted with userland allowed you to run basic homebrew and emulators but did not allow you to (easily) modify games or dump cartridges. It was also a lot less stable, with homebrew often ungracefully crashing and requiring a full reboot. Custom firmware grants a far greater level of system access while also being more stable than homebrew-only entrypoints.

:::

## Post-Installation FAQ

::: details Is it safe to update my 3DS to the latest version with CFW?

If you are using Luma3DS, your custom firmware loader (boot9strap) will *never* be removed when performing a system update. There have been updates in the past that have resulted in Luma3DS crashing on boot, so it is a good idea to wait a couple of hours to ensure that the latest update will not temporarily render the console unusable until Luma3DS is updated. System updates can be performed the same way as they are on an unmodified 3DS: through System Settings, Safe Mode, or the update prompt when the update is automatically downloaded.

:::

::: details How do I upgrade my SD card?

Copy and paste your SD card contents to a new SD card formatted as FAT32. For 128GB cards, an allocation size of 65536 is recommended. SD cards larger than 128GB are not recommended due to known issues with GBA graphics and custom themes.

:::

::: details Can I system transfer with CFW?

Yes, system transfers can be performed through the official System Transfer function to other consoles with CFW (inconsistencies may occur if the target console is unmodified). Tickets for illegitimate titles (homebrew) will not transfer, but the titles can be made to reappear with [faketik](https://github.com/ihaveamac/faketik/releases/latest). Make sure that you do not perform a wireless transfer, as this will delete illegitimate titles. CFW will remain on both consoles.

:::

::: details How do I change the system language of a Japanese 3DS?

The only way to change the system language of a Japanese 3DS to a language other than Japanese is to perform a [region change](region-changing). Note that this is very likely to break the Nintendo eShop on your console, which means you will be unable to update your games whether they are in-region or out-of-region.
 
:::

::: details How do I update homebrew applications?

It depends on the format of the homebrew application. Generally speaking:

* Homebrew in **CIA format** can be updated by installing the new CIA, which will usually overwrite the old one. If the old CIA is not overwritten, you can delete the old one from Data Management as you would any other 3DS title.
* Homebrew in **3DSX format** can be updated by replacing the 3DSX file in `/3ds/` with a fresh copy. If the homebrew application includes additional assets, you may need to place that folder somewhere else. Refer to the documentation of the homebrew application.
* For updating Luma3DS, see [this page](restoring-updating-cfw). For updating GodMode9, see [this page](godmode9-usage#updating-godmode9).

:::

::: details How do I update my games?

You can continue to download game updates from the Nintendo eShop, even though it has now shut down.

If the game is not from the same region as the console, you will need to [dump the updates](dumping-titles-and-game-cartridges) from a 3DS that has the updates installed. The Nintendo eShop only contains updates for the console's region (for example, a Japanese 3DS will only have updates for Japanese games).

:::

::: details Help! Something bad happened and my 3DS won't boot to HOME Menu...

Please look at the [troubleshooting guide](troubleshooting-post-install). **Uninstalling CFW when your console is in an unbootable state is not recommended, as it is very likely to lead to a brick**.

:::

## menuhax / A9LH / Gateway FAQ

::: details I modded my console (x) years ago, so it already has some sort of homebrew. What should I do?

It is recommended that you upgrade your setup to a modern, boot9strap-based one. Follow the [Checking for CFW](checking-for-cfw) guide to see how to upgrade your setup.

:::

::: details My setup works for me. Why should I upgrade it?

The vast majority of modern homebrew (such as Checkpoint and BootNTR Selector) have only been tested on modern, boot9strap-based setups and may not work entirely (or at all) on older setups based on menuhax, A9LH, or Gateway. In addition, depending on your setup, you may be unable to safely update to the latest firmware. Modern, boot9strap-based setups allow for a greater level of system access than previous hacks, including the ability to dump your console's bootrom.

:::

::: details Will I lose anything if I upgrade my setup?

Your old setup (including your EmuNAND, if you have one) can usually be directly migrated to boot9strap with no data loss. If you have data that is particularly important to you, it would be a good idea to make a decrypted backup of your save data before upgrading your setup with a tool like [JKSM](https://github.com/J-D-K/JKSM/releases/tag/12%2F20%2F2018).

:::

::: details How do I move saves from an existing Gateway setup to a more modern setup?

See [this thread](https://gbatemp.net/threads/425743/).

:::
