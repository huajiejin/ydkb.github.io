# Atmel DFU Bootloader

This is the default bootloader for some AVR microcontrollers. It is used directly by many keyboards not produced by ydkb.


## Install DFU driver using Zadig

The driver of this DFU is in the same computer and system, it only needs to be installed once, the next time you flash the firmware, you can start directly from step 2. If the keyboard of this Bootloader has been used to refresh the keyboard on this computer, then there is already a driver, no need to reinstall it.

### 1 Download Zadig

To use this bootloader to reflash the firmware, you must install the driver. Use zadig from http://zadig.akeo.ie. 

### 2 Get the keyboard into DFU mode

First plug the keyboard into the USB, and then press the flash button. For the specific location of the keyboard, refer to the instructions of the corresponding keyboard. Generally, it is a small button on the keyboard PCB.

> [!ydda] ATTENTION
> - Be sure to press the flash button to let the keyboard enter the DFU mode.
> - If you install a driver for a device other than DFU, the keyboard may become unusable.

From the list below, find **ATm32U4DFU** or **LUFA DFU**. 

```ad-yddcol0
##### ATm32U4DFU
![](assets/atmel_dfu_01.png)
```

```ad-yddcol1
##### LUFA DFU
![](assets/atmel_dfu_lufa_01.png)
```

> [!ydda] ATTENTION Again.
> - Don’t choose GH60 or other keyboard name</font></html>, If you choose and install this driver, the keyboard will not work. Then you need to uninstall the driver manually.

![|600](assets/atmel_dfu_02.png)


### 3 Intall driver

After choosing **ATm32U4DFU** or **LUFA DFU**, click "Install Driver" to make its driver be WinUSB.

![](assets/atmel_dfu_03.png)

As shown above, the Driver is already displayed as WinUSB, indicating that the installation was successful. 

> [!yddh] HINT
> - If the installation is not successful, try again or try running zadig.exe as an administrator.

### 4 Additional instructions

If still unsuccessful, it may because that windows system is a lited one and misses the support for WinUSB. In that case, you can choose to install the LibUSB driver. The reflash tool provided by YDKB supports both LibUSB and WinUSB drivers.

> [!yddh] If you have other keyboards with ATMEL DFU Bootloader
> - If you have other keyboards using tkg.io, it is recommended to install the WinUSB driver, because tkg uses that.
> - If you have other keyboards using qmk, it is recommended to install the LibUSB driver. The qmk firmware reflash tool uses LibUSB.

## Flash HEX firmware

Use the keyboard of Atmel DFU Bootloader, the general firmware format is HEX, drag the HEX file directly to YDKB Tool.exe in the flashing tool (there is the downloading flashing tool at the location where the hex firmware is downloaded), and the flashing will start. It should be noted that when YDKB Tool is decompressing, all contents need to be decompressed and kept in the same folder. Do not move files or modify the file names of the files.

![|600](assets/dfu_reflash_01.png)

Then it will prompt "the device will automatically recognize and execute the update after entering the flashing mode". At this time, press the flashing button of the keyboard, or press the flashing button in advance to put the keyboard in the flashing mode, and it will automatically start to refresh. As shown in the figure below, DFU is recognized and the firmware is updated.

![|600](assets/dfu_reflash_02.png)


