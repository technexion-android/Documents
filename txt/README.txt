*****************************************************
* Author: Technexion                                *
*                                                   *
* Date: 2020/11/09                                  *
*                                                   *
* Title: Android 10 Runtime image README file       *
*                                                   *
*****************************************************

# User Manual:
Android-Pie_Release-Note_20190920.pdf (Android 10 will be updated soon)

# Release Note:
Android-Pie_User-Manual_201900920.pdf (Android 10 will be updated soon)

# Github SDK:
https://github.com/technexion-android/cookers/tree/tn-android-10.0.0-2.5.0_8m-next

# UUU tool (recommend 1.4.43 revision)
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

  Please change the boot mode to seiral download mode first, then connect a OTG cable from board to host PC, then issue command:

	Linux host: sudo ./uuu_imx_android_flash.sh -c <eMMC size> -f <cpu name> -e -D . -super
	Windows host: uuu_imx_android_flash.bat -c <eMMC size> -f <cpu name> -e -D . -super

	eMMC size: 9GB -> 9 (for qucik testing), 16GB -> 13, 32GB -> 28
	cpu_name: edm-g-imx8mp -> imx8mp
