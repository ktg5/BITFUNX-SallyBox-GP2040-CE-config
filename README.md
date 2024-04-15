# BITFUNX-SallyBox-GP2040-CE-config
This is repo for those that use the BITFUNX SallyBox & want to upgrade their device to the latest GP2040-CE release.

# Setup
If you have any issues with any part of this guide, [please open up a issue](./issues) and I'll be happy to help.

## Backing up the current settings
1. Load your SallyBox into Web Config mode by holding down the START button at the top right of the controller **and** either unplug & plug in the USB cable to the device or use the red reset button at the top of the controller.
2. Open a new browser tab & enter `192.168.7.1`.
3. Note down the current version of the GP2040-CE firmware you're using.
4. At the top of the page, go to `Configuration` > `Data Backup and Restoration`.
5. In the `Backup To File` section of the backup page, make sure **all** options are enabled and click on `Save`. When the website asks you to save the file, I recommend naming the file something like `SallyBox-GP2040-CE-config-(version number that was noted down)`. Save this file somewhere safe, as you can go back to this file if you have the version that it was used on.

Continue to the next step if you're reading through the entire setup process.

## Installing the new firmware
1. Download `flash_nuke.uf2` & `GP2040-CE_x.x.x_RP2040AdvancedBreakoutBoard.uf2` from [the latest GP2040-CE release](https://github.com/OpenStickCommunity/GP2040-CE/releases/latest). Also [download the custom config from this repo](./SallyBox-GP2040-CE-config.gp2040).
2. Make sure your SallyBox is in Web Config mode. To do so, hold down the START button at the top right of the controller **and** either unplug & plug in the USB cable to the device or use the red reset button at the top of the controller.
3. Open a new browser tab & enter `192.168.7.1`.
4. At the top right of the page, there should be a `Reboot` button. Click on it and select `USB (BOOTSEL)`.
5. Once the SallyBox has rebooted, open your file manager and go to the SallyBox device which might have something with `RP2` as it's name. (for Windows normies, open File Explorer if a window showing the device hasn't showed up & look a USB drive with `RP2` in it's name).
6. Copy the `flash_nuke.uf2` to the `RP2` drive. Wait for the SallyBox to reconnect to your computer.
7. Copy the `GP2040-CE_x.x.x_RP2040AdvancedBreakoutBoard.uf2` to the same drive.

Once the copy is done & the SallyBox has rebooted, **we still need to copy the config so that the buttons aren't screwed up**.

8. Hold down the `LB` button on the SallyBox **and** either unplug & plug in the USB cable to the device or use the red reset button at the top of the controller. We'll be loading into Web Config mode again, but since our config has been reset, the button is different.
9. Open a new browser tab & enter `192.168.7.1`.
10. At the top of the page, go to `Configuration` > `Data Backup and Restoration`.
11. In the `Restore From File` **don't use your backed up config, as it'll need some manual configuration**. Instead, use the custom config from this repo you downloaded before. (Which you did do, right?)

Now your SallyBox should be on the latest version of GP2040-CE & be fully functional. If you'd like to mess around with the config, such as change the logo, or change the custom theme, be my guest!

As said before; if you have any issues with any part of this guide, [please open up a issue](./issues) and I'll be happy to help.