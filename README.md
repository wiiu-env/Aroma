# Aroma Environment

This is a environment to be loaded with the [EnvironmentLoader](https://github.com/wiiu-env/EnvironmentLoader).

It's recommended to coldboot into EnvironmentLoader (and Aroma) via the [PayloadLoader](https://github.com/wiiu-env/PayloadLoaderInstaller). Check the repository out for more information.

# What is Aroma?
Aroma is a collection of tools for using homebrew on the Wii U.

## Features
Aroma's tools, modules and plugins are modular, meaning that features can easily be added or removed.

A default Aroma instance comes with the following features:
- Compatibility with the latest firmware (5.5.5/5.5.6).
- Free and persistent entrypoint (including an installer + coldboot option)
- Compatible with existing entrypoints (browser exploit)
- Easy setup and update: Just copy the files to the SD card.
- Built-in support for modules 
- Built-in integration of the Wii U Plugin System
- All modules and plugins use a seperate memory heap to improve stability
- Plugins and homebrew applications can be used at the same time.

These basic features can be easily extended by plugin. Common plugins are:
- [homebrew_on_menu_plugin](https://github.com/wiiu-env/homebrew_on_menu_plugin): Load homebrew directly from the Wii U Menu instead of using a dedicated homebrew launcher.
- [ftpiiu_plugin](https://github.com/wiiu-env/ftpiiu_plugin): Run a FTP server in the background.
- [wiiload_plugin](https://github.com/wiiu-env/wiiload_plugin): Wiiload support: Launch homebrew/plugin via the network at any time.
- [drc_region_free_plugin](https://github.com/wiiu-env/drc_region_free_plugin): Pair game pads from different regions
- [region_free_plugin](https://github.com/wiiu-env/region_free_plugin): Launch games from different regions.

## Download

A bundle with the latest files can be downloaded [here](https://aroma.foryour.cafe/package/base-aroma) by clicking on "Download all".

## Usage

1. Extract the files to the root of your sd card
2. Launch the environment via the [EnvironmentLoader](https://github.com/wiiu-env/EnvironmentLoader). You may need to hold `X` while launching the EnvironmentLoader to force open the menu.

## Troubleshooting SD card write errors

If Aroma reports that the SD card is write-locked even though other Wii U software can still write to the card, check the SD card's physical lock tab (or the tab on a microSD-to-SD adapter) first.

If the physical lock is not the cause, recreate the Aroma files on the SD card from fresh downloads instead of reusing the existing `wiiu` tree. On Windows, files or directories copied or extracted to FAT32 media can retain attributes that make the `wiiu` tree effectively read-only to Aroma. Re-extract the current Base Aroma and payload archives with an archive tool such as 7-Zip, then retry before restoring unrelated homebrew files.

A successful write from Mii Maker does not prove that Aroma's `wiiu` directory is writable, because it writes elsewhere on the card. If the problem persists with freshly downloaded files on known-good media, treat it as a separate filesystem, adapter, SD-slot, or hardware problem rather than repeatedly modifying the Aroma installation.

## Where's the Code?

Aroma is a collection of tools, which all have public repos.

You can go to https://aroma.foryour.cafe/package/base-aroma and click on any listed repository to see the source code of each part.
