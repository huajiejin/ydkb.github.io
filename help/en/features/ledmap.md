# LEDMAP

Most of the indicator functions of the keyboard supported by YDKB can be customized.


## Kinds of indicators

If the keyboard supports the LEDMAP function, a **[ LEDMAP]** label is displayed at the end of the selected layer.

```ad-yddcol0
![](assets/ledmap_01.png)
```

```ad-yddcol1
![](assets/ledmap_03.png)

There are two kinds of indicators.


| Kind??30% | Description |
| --- | --- |
| Monochrome | Only functions can be set. In addition, a certain color of RGB is also set as a monochrome indicator |
| RGB | in addition to setting the indicator function, you can also specify the color. |
| Undefinable indicator | This part, such as the charging indicator, also has some specific purposes. It does not support modification in the LEDMAP. It also has a specific indication function. |

> [!yddh] HINT
> - The LEDMAP of some keyboards supports setting RGB bottom light and backlight, but they can only take effect as LEDMAP indicator functions when the RGB lighting effect and backlight are turned off.


## Functions of indicator 

![|600](assets/ledmap_02.png)

Currently supports up to 8 indicators, each indicator can be individually assigned its function, the supported function is in its drop-down list. There will be instructions when the mouse is pointed.

| Function??30% | Description |
| --- | --- |
| Unconfigured | That is, do not set this indicator, keep it as default. |
| Disable | Used to set some backlight and RGB lights. Not installed or do not want to use select this option, more energy saving. |
| Num Lock<br>Caps Lock<br>Scroll Lock | Traditional keyboard status indicator <html><br></html> It should be noted that the Bluetooth mode is not synchronized with the system. <html><br></html>For details, please refer to the last description of this page. |
| Win Lock | Used with corresponding functions, lights up when the Win key is locked |
| Layer 1...7 | When the setting layer is open, the indicator lights up |
| Default Layer 1...7  | When the current default layer is the set value, the indicator lights up |
| 工作模式(部分键盘有) | USB connection when the indicator light is on, Bluetooth when it is off |
| 接蓝牙模块(部分键盘有) | Part of the keyboard connected to the Bluetooth module needs to occupy the IO of the LED light, and this needs to be set|
| WS2812 RGB(部分键盘有) | Some keyboards use RGB lights to occupy the IO of the LED lights, and this needs to be set |



## Indicator in bluetooth mode

> [!ydda] ATTENTION when in bluetooth mode
> - In bluetooth mode，The Num, Caps, and Scroll Lock indicators are not synchronous with the OS status in Bluetooth mode. 
> - In bluetooth mode, They just toggle on or off when pressed. They are synchronous in USB mode.
> - If one indicator is out of sync, you can use Shift + KEY, such as Shift + Capslock. In this way CapsLock will take effect but its indicator won't change.
> - Reasonable use of this in bluetooth mode to reverse the indicator light, such as turning off the numlock light when numlock is on and light on when it is off, which can save power.

