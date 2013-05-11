###Details###

mpr-a1-16m-luci-usb-mjpg.bin - (openwrt firmware,16M RAM)

mpr-a1-32m-luci-usb-mjpg.bin - (openwrt firmware,32M RAM)

hame-mpr-a1-v22.bin - （hame-mpr-a1 4M Hame origin firmware）

hame-mpr-a1-v22-uboot128.bin - （HAME Uboot support16MRAM, divide from hame-mpr-a1-v22.bin） 

uboot256.img - (RT5350 32M RAM Uboot，support 32M RAM)

openwrt-hlk-rm04-4m-16m-luci-usb-mjpg.bin - (HiLink HLK-RM04 4M openwrt bin file with uboot and other all things, 16M SDRAM version)

openwrt-hlk-rm04-4m-32m-luci-usb-mjpg.bin - (HiLink HLK-RM04 4M openwrt bin file with uboot and other all things, 32M SDRAM version)

hlk-rm04-16m-luci-usb-mjpg.bin - (HiLink HLK-RM04 openwrt bin file, 16M SDRAM version only openwrt firmware)

hlk-rm04-32m-luci-usb-mjpg.bin - (HiLink HLK-RM04 openwrt bin file, 32M SDRAM version only openwrt firmware)

###SDRAM###
	Micron        32M     mT48LC16m16A2 
	EtronTech     32M     EM63A165
	ESMT          32M     M12L2561616A

###RESOURCE###

#####WIKI#####
[Hame MPR-A1](http://wiki.openwrt.org/toh/hame/mpr-a1)

[HiLink HLK-RM04](http://wiki.openwrt.org/toh/hilink/hlk-rm04)

#####Forum#####
[Hi-Link wireless module HLK-RM04](https://forum.openwrt.org/viewtopic.php?id=42142)

[HAME MPR-A1 - Small and cheap router with built-in battery](https://forum.openwrt.org/viewtopic.php?id=37002)

#####OTHERS#####
[Squonk42's RT5350](https://github.com/Squonk42/OpenWrt-RT5350?source=cc)

###How To###

###Note###

LUCI runs very slowly with 16M SDRAM. Strongly recommend to upgrade the SDRAM to 32M
