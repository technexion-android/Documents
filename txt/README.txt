*****************************************************
* Author: Technexion                                *
*                                                   *
* Date: 2019/08/19                                  *
*                                                   *
* Title: Android 9 Runtime image README file        *
*                                                   *
*****************************************************

# User Manual:
Android-Pie_Release-Note_20190725.pdf

# Release Note:
Android-Pie_User-Manual_201900807.pdf

# Github SDK:
https://github.com/technexion-android/cookers/tree/tn-p9.0.0_2.0.0_8m-ga

# UUU tool (recommend 1.2.91 revision)
https://github.com/NXPmicro/mfgtools/releases

# UUU User Manual
UUU.pdf

# UUU environment settings
Please refer to the Android-Pie_User-Manual chapter 5

# Use zadig to install winusb driver
Please refer to the UUU.pdf chapter 7.3
zadig-2.4.exe

Flashing the images:

uuu release:
	Linux host: sudo ./uuu_imx_android_flash.sh -c <eMMC size> -f <cpu name> -e -D .
	Windows host: uuu_imx_android_flash.bat -c <eMMC size> -f <cpu name> -e -D .

	eMMC size: 8GB -> 7, 16GB -> 13, 32GB -> 28
	cpu_name: imx8mq / imx8mm

dd image release: (cpu_name: imx8mq)
	Linux host: method 1: sudo dd if=xxx.img of=/dev/sdx bs=1M (use ums or mfgtools to mount as storage first)
		    method 2: uuu -b emmc_all imx-boot-pico-imx8mq-sd.bin xxx.img
	Windows host: uuu -b emmc_all imx-boot-pico-imx8mq-sd.bin xxx.img

dd image release: (cpu_name: imx8mm)
        Linux host: method 1: sudo dd if=xxx.img of=/dev/sdx bs=1M (use ums or mfgtools to mount as storage first)
                    method 2: uuu -b emmc_all imx-boot-pico-imx8mm-sd.bin xxx.img
        Windows host: uuu -b emmc_all imx-boot-pico-imx8mm-sd.bin xxx.img
