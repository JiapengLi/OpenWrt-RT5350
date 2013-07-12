##Details##

These bins were compiled under trunk reversion 35407, MPR-A1 files was compiled by using [Squonk42's RT5350 patch](https://github.com/Squonk42/OpenWrt-RT5350?source=cc). ***LUCI runs very slowly on 16M SDRAM hardware.***

	mpr-a1 related bins are in **mpr-a1**.
	
	hlk-rm04 relate bins are in **hlk-rm04**
	
	**u-boot** contains the RT5350 u-boot image.

mpr-a1-16m-luci-usb-mjpg.bin - (openwrt firmware,16M RAM)

mpr-a1-32m-luci-usb-mjpg.bin - (openwrt firmware,32M RAM)

hame-mpr-a1-v22.bin - （hame-mpr-a1 4M Hame origin firmware）  
*MAC: 9C417CE21C58  
WIFI NAME: HAME_A1_21C5  
WIFI PASSWORD: 7ce21c58*  

hame-mpr-a1-v22-uboot128.bin - （HAME Uboot support16MRAM, divide from hame-mpr-a1-v22.bin） 

uboot256.img - (RT5350 32M RAM Uboot，support 32M RAM)

openwrt-hlk-rm04-4m-16m-luci-usb-mjpg.bin - (HiLink HLK-RM04 4M openwrt bin file with uboot and other all things, 16M SDRAM version)

openwrt-hlk-rm04-4m-32m-luci-usb-mjpg.bin - (HiLink HLK-RM04 4M openwrt bin file with uboot and other all things, 32M SDRAM version)

hlk-rm04-16m-luci-usb-mjpg.bin - (HiLink HLK-RM04 openwrt bin file, 16M SDRAM version only openwrt firmware)

hlk-rm04-32m-luci-usb-mjpg.bin - (HiLink HLK-RM04 openwrt bin file, 32M SDRAM version only openwrt firmware)

### SDRAM

If you want to run LUCI on HLK-RM04 or MPR-A1, you may want to expand the 16M SDRAM to 32M, here is some available 32M SDRAM chips.

	Micron        32M     mT48LC16m16A2 
	EtronTech     32M     EM63A165
	ESMT          32M     M12L2561616A

### RESOURCE

#### WIKI
[Hame MPR-A1](http://wiki.openwrt.org/toh/hame/mpr-a1)

[HiLink HLK-RM04](http://wiki.openwrt.org/toh/hilink/hlk-rm04)

#### Forum
[Hi-Link wireless module HLK-RM04](https://forum.openwrt.org/viewtopic.php?id=42142)

[HAME MPR-A1 - Small and cheap router with built-in battery](https://forum.openwrt.org/viewtopic.php?id=37002)

#### OTHERS
[Squonk42's RT5350](https://github.com/Squonk42/OpenWrt-RT5350?source=cc)

## PATCH
Usage:  

	mkdir openwrt
	cd openwrt
	svn co svn://svn.openwrt.org/openwrt/trunk
	git clone https://github.com/Squonk42/OpenWrt-RT5350.git
	cd trunk
	patch -p0 <../OpenWrt-RT5350/openwrt_add_pm25lq032_flash_support.patch
	patch -p0 <../OpenWrt-RT5350/openwrt_add_rt5350_wlan_support.patch
	patch -p0 <../OpenWrt-RT5350/openwrt_hame_mpr-a1.patch
	make menuconfig


## How To
####Possible way to flash MPR-A1 (without using serial)####
Use the tools(for Windows) in **tools/Hame** to upgrade Hame. 

**BE CAREFUL,THESE PROCEDURE IS NOT TESTED.**

These tools from hame is in Chinese. Fortunately, however, it's very simple.

-1.Close your Hame device, disconnect your Hame device with your PC.

0.If your OS is WIN7, install **vcredist_x86.exe** first

1.Set your IP address to **192.168.1.55**, sub-mask **255.255.255.0**, GateWay **NULL**

2.Start up **OneKeyUpgrade.exe**, select your *OpenWrt bin file*.

3.Checked the **"升级Root_uImage"**. 

4.Click the **"启动"** button.

5.Keep pressing the **Reset** button, and start your **Hame device**, you can see the blue LED long bright.

6.Connect your Hame with your PC, connection can be created automatically, and upgrade starts.

7.During the flashing, red LED is always lighting. After Hame device have been flashed, it will restart automatically.

8.After all things, you can see a dialog with these strings **"设备写入完成，可以移除"** is popped up. This means you are successful.

**9.WARNING: because my hame MPR-A1 has been flashed to OpenWrt, so i don't test it.**

*Last, if someone has tested this, please feed me back no matter failed or successful.*

Thank [xajialuo](http://www.right.com.cn/forum/space-uid-81425.html) from [恩山wifi论坛](http://www.right.com.cn/forum/forum.php) for finding these tools. 

## Note

LUCI runs very slowly with 16M SDRAM. Strongly recommend to upgrade the SDRAM to 32M
