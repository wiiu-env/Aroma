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

## Where's the Code?

Aroma is a collection of tools, which all have public repos.

You can go to https://aroma.foryour.cafe/package/base-aroma and click on any listed repository to see the source code of each part.
