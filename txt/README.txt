*****************************************************
* Author: Technexion                                *
*                                                   *
* Date: 2021/03/30                                  *
*                                                   *
* Title: Android 11 Runtime image README file       *
*                                                   *
*****************************************************

# User Manual:
Android-Pie_Release-Note_20190920.pdf (Android 11 will be updated soon)

# Release Note:
Android-Pie_User-Manual_201900920.pdf (Android 11 will be updated soon)

# Github SDK:
https://github.com/technexion-android/cookers/tree/tn-android-11.0.0-1.2.0_8m-next

# UUU tool (recommend 1.4.72 revision)
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


flash 16GB size image to eMMC:

	Linux host: sudo ./uuu_imx_android_flash.sh -f <cpu name> -e -D .
	Windows host: uuu_imx_android_flash.bat -f <cpu name> -e -D .

flash 32GB size image to eMMC:

	Linux host: sudo ./uuu_imx_android_flash.sh -c 28 -f <cpu name> -e -D .
	Windows host: uuu_imx_android_flash.bat -c 28 -f <cpu name> -e -D .


cpu_name: edm-g-imx8mp -> imx8mp
