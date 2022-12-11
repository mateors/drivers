# LINUX DEVICE DRIVERS

## Kernel
The kernel is the big chunk of executable code in charge of handling system resources(omputing power, memory, network connectivity etc) requests.

## Classes of Devices and Modules
The Linux way of looking at devices distinguishes between three fundamental device types. Each module usually implements one of these types

1. char module
2. a block module 
3. a network module. 

## Character devices
> A character (char) device is one that can be accessed as a stream of bytes (like a file); a char driver is in charge of implementing this behavior. Such a driver usually implements at least the open, close, read, and write system calls. The text console (/dev/console) and the serial ports (/dev/ttyS0 and friends) are examples of char devices, as they are well represented by the stream abstraction. 

> Char devices are accessed by means of filesystem nodes, such as /dev/tty1 and /dev/lp0. The only relevant difference between a char device and a regular file is that you can always move back and forth in the regular file, whereas most char devices are just data channels, which you can only access sequentially

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
