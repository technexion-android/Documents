*****************************************************
* Author: Technexion                                *
*                                                   *
* Date: 2019/09/19                                  *
*                                                   *
* Title: Android 9 Runtime image README file        *
*                                                   *
*****************************************************

# User Manual:
Android-Pie_Release-Note_20190725.pdf
PreBuilt_OS_Image_Installation_Guide_v3.5.pdf

# Release Note:
Android-Pie_User-Manual_201900807.pdf

# Github SDK:
https://github.com/technexion-android/cookers/tree/tn-p9.0.0_2.2.0-ga

# Use USB-OTG intaller tool to program eMMC tool
ftp://ftp.technexion.net/development_resources/development_tools/installer/pico-imx6-imx6ul-imx7_otg-installer_20171101.zip

Flashing the images:

dd image release:
	Linux host:
		Use ums or mfgtools to mount as storage first
		Please refer to the PreBuilt_OS_Image_Installation_Guide_v3.5.pdf chapter 6.2
		sudo dd if=xxx.img of=/dev/sdx bs=1M oflag=dsync

	Windows host:
		Use ums or mfgtools to mount as storage first
		Please refer to the PreBuilt_OS_Image_Installation_Guide_v3.5.pdf chapter 6.1
		Execute Win32DiskImager.exe
