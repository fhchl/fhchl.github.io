<!--
.. title: Windows 10 and Ubuntu
.. slug: windows-10-and-ubuntu
.. date: 2018-06-06 17:14:40 UTC+02:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
.. status: draft
-->

### Make bootable USB sticks

Install WoeUSB

	sudo add-apt-repository ppa:nilarimogard/webupd8
	sudo apt-get update
	sudo apt-get install woeusb

Unmount devices

	sudo fdisk -l # find it
	sudo umount -A /dev/sdb1

Install with WoeUSB

	sudo woeusb --workaround-bios-boot-flag --device Downloads/en_windows_10_education_version_1703_updated_march_2017_x86_dvd_10188968.iso /dev/sdb 


