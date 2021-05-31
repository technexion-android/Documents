*****************************************************
* Author: Technexion                                *
*                                                   *
* Date: 2021/05/31                                  *
*                                                   *
* Title: Android 11 UUU installer README file       *
*                                                   *
*****************************************************

# Release Note:
https://developer.technexion.com/docs/android-11-release-notes

# Github BSP source code:
https://github.com/technexion-android/cookers/tree/tn-android-11.0.0_1.2.0_8m-next

# Download UUU tool (revision 1.4.72 or above is necessary, adapt 1.4.72 as example)

Ubuntu host:
	https://github.com/NXPmicro/mfgtools/releases/download/uuu_1.4.72/uuu
Windows 10 host:
	https://github.com/NXPmicro/mfgtools/releases/download/uuu_1.4.72/uuu.exe

# UUU User Manual
https://github.com/NXPmicro/mfgtools/releases/download/uuu_1.4.72/UUU.pdf

# UUU environment settings

Ubuntu Host:
	$ sudo a+x uuu
	$ sudo mv uuu /usr/bin/
	$ uuu -v 
	uuu (Universal Update Utility) for nxp imx chips -- libuuu_1.4.72-0-g8e9e189

Windoes 10 Host:
	1. Download VS2017 Redistribute Package for USB relate drivers: https://go.microsoft.com/fwlink/?LinkId=746572
	2. Install VS2017 Redistribute Package
	3. open 'cmd' tool with administrator permission
		C:\Windows\system32> cd c:\
		> mkdir utility
		> copy uuu.exe utility
		> set PATH=%PATH%;c:\utility 

Flashing the images:

uuu release:

  Please change the boot mode to seiral download mode first, then connect a OTG cable from board to host PC, then issue command:


flash image to eMMC:

Ubuntu  host:
	$ sudo ./uuu_imx_android_flash.sh -f <cpu name> -e -D .

Windows 10 host (remember close VMware/VirtualBox first is necessary to avoid USB stuck in virtual machine):
	> uuu_imx_android_flash.bat -f <cpu name> -e (sometimes need press enter if stuck "This script is validated ....")

cpu_name: edm-g-imx8mp -> imx8mp, pico-imx8mm -> imx8mm

if you want to change image size: 14GiB -> -c 14, 32GiB -> -c 28
