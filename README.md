# LINUX DEVICE DRIVERS



### What is the difference between character and block device drivers in UNIX?

They are two main types of devices under all Unix systems:

A Character Device is a device whose driver communicates by sending and receiving single characters (bytes, octets). Example - serial ports, parallel ports, sound cards, keyboard.

A Block Device is a device whose driver communicates by sending entire blocks of data. Example - hard disks, USB cameras, Disk-On-Key.

(Note: Filesystems can only be mounted if they are on block devices.)

The sources for character devices are kept in drivers/char/, and the sources for block devices are kept in drivers/block/.


## Learning Resource

* http://csapp.cs.cmu.edu/
* https://medium.com/swlh/7-steps-i-follow-for-developing-a-device-driver-bd1019e40b07
* https://lwn.net/Kernel/LDD3/
