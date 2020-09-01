## Linux Kernel Configuration for Nunchuk device

This implementation follows the labwork of an open source training **'Linux kernel and driver development'** from Bootlin.

https://bootlin.com/doc/training/linux-kernel/linux-kernel-slides.pdf

https://bootlin.com/doc/training/linux-kernel/linux-kernel-labs.pdf

The hardware used for this project is **BeagleboneBlack**(http://beagleboard.org/black). This branch has the kernel configuration for enabling ports so that the Nunchuk() can be used as an I2C device. The configuration file can be found in https://github.com/ranjithasubramaniam/Linux-Kernel-and-Driver-Development-Nunchuk-Kernel-Config/blob/nunchuk/arch/arm/boot/dts/am335x-customboneblack.dts

In order to facilitate continuous development of the nunchuk device driver, the driver is compiled as a standalone (out-of-tree) kernel module. The driver is developed in the host system and deployed to the target system using NFS(Network File System) root filesystem. Once the developement is frozen, the device driver will be moved to this repository as in-tree kernel module. 

The current status of the device driver for Nunchuk can be found in the link:
https://github.com/ranjithasubramaniam/Linux-Kernel-and-Driver-Development-Custom-Drivers/tree/master/nfsroot/root/nunchuk/nunchuk.c

