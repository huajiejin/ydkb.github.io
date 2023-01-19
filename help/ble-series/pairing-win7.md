# Win7 配对 BLE 设备

> [!ydda] 注意
> - Win7发布早于蓝牙4.0，且微软一直未更新win7支持蓝牙4.0
> - 要在Win7下使用蓝牙4.0的键盘，必须使用第三方驱动。
> - 如果非必要，建议更新到Win10；如果一定要Win7下使用，往下继续看。

## Intel 的蓝牙硬件

虽然现在有的Intel硬件已经不支持安装Win7了，但依然还是有一些支持的。查询你的无线网卡是Intel的话，那么一般Intel官网可能也有提供Win7的蓝牙驱动。据用户回复说，Intel的官方驱动在Win7下安装上就可以使用BLE的设备了。


## CSR8510 芯片蓝牙接收器

大部分人使用的蓝牙4.0适配器应该是CSR8510这个芯片的，淘宝上从10几块到4、50块的价格都有，没太大的区别。

第三方驱动使用千月。

> [!yddh] 提醒
> - 千月是收费的，淘宝上单机的注册码17.9元。也可以直接买本身有授权的蓝牙适配器。
> - 如果未注册，无法使用千月的蓝牙4.0低功耗设备管理功能。

### 1 安装千月

安装的时候插着蓝牙适配器或者安装完成后都成。

```ad-yddcol0
1. 请从官网下载运行安装软件。

![](assets/qy01.jpg)
```

```ad-yddcol1
2. 这个手机助手可以不装。

![](assets/qy02.jpg)
```

### 2 连接键盘

安装完成后按要求重启，然后开始连接键盘。

```ad-yddcol0
1. 从托盘菜单里看到蓝牙图标，要启动的是那个蓝牙4.0低功耗管理。

![](assets/qy07.jpg)

> [!ydda] 注意
> - 一定要从这里启动才是低功耗设备管理。
> - 千月必须是激活的版本才有这个选项。
```


```ad-yddcol1
2. 然后在其他 — HID里，添加设备，并且连接。

![](assets/qy08.jpg)

3. 成功搜索到蓝牙，正常应该就能用了，如果还是不能，再往下看。
```

### 3 能连上但不能用

连上后可能不能用。那么请根据下面的说明，指定安装蓝牙HID的驱动。

```ad-yddcol0
1. 查看设备管理器，这里可能是个问号。

![](assets/qy09.jpg)

2. 即使不是问号，如果不能使用，一样右键点击它，选择更新驱动。

![](assets/qy10.jpg)

3. 选择“浏览器计算机以查找驱动程序软件”，再选择“从计算机的设备驱动程序列表中选择”。

![](assets/qy11.jpg)

```

```ad-yddcol1
4. 然后取消掉下图中的勾，选择列表里红框项。

![](assets/qy12.jpg)

5. 会有如下提示，无视就行了。

![](assets/qy13.jpg)

6. 直接点击是，然后会安装新的驱动，安装后会提醒需要重启，但其实这时已经可以使用了。当然最好还是再重启一下。

![](assets/qy14.jpg)

```

我测试时因为电脑非常慢，重启后在登录界面，键盘是不可用的，但有其他用户表示登录界面是可以使用的。

进入系统待千月启动好了后，键盘会自动连接上，直接可用无问题。


## 其他方法
Win7也可以使用Niz的接收器（移步 [Niz蓝牙4.0键盘接收器](ble-series/pairing-niz-dongle.md) 查看）。
