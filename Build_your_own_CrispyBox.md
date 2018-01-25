# Building your own CrispyBox
You'll need to build CrispyBox yourself if want/need to:
* use a non-Debian-based Linux distribution
* use a cloud provider other than Dropbox
* have more than a maximum of 10GB (9GB for Dropbox) available for storage
* use a fixed HDD instead of a dynamic HDD
* use a swap partition
* just have alot of fun!

## Building a standard CrispyBox
*These instructions will build a standard CrispyBox, version 0.9.5-beta-standard+180125*

### Requirements
The standard build of CrispyBox has the following minimum requirements:
* A Linux operating system installation ISO
* Virtualization software
* A working knowledge of the Linux command line
* An internet connection
* About 30 minutes

### Recommendations
The standard build of CrispyBox has the following recommendations:
* [Debian linux](https://www.debian.org), version 9.3.0 [network install ISO](https://www.debian.org/CD/netinst/).
* Use a 32-bit operating system, unless you have a specific need for 64-bit.
* [Oracle VirtualBox](https://www.virtualbox.org/), version [5.2.6](http://download.virtualbox.org/virtualbox/5.2.6/).

These instructions will need to be modified if the above recommendations are not met.

### Creating the virtual machine
The minimum specifications of an CrispyBox virtual machine are:
> * 1 CPU
> * 512MB RAM
> * 16MB VRAM
> * 10GB Dynamic HDD
> * Bridged networking

### Installing the base operating system
These instructions are for Debian, using the "Advanced options > Expert install" installation options. If you are using another operating system, try and mirror these as much as possible.

Just take the default options for each choice, except for the following:
> * USB-storage driver: unchecked
> * Hostname: CrispyBox
> * Root user: no
> * Create normal account: crispy/crispy
> * Partition disk: use entire disk, create one partition, no swap partition, msdos format
> * Kernel: non-meta 686 
> * Drivers: Targeted
> * Use non-free software: Yes
> * Enable source repositories: Yes
> * Backported software: checked
> * virtualbox-ose-guest-x11: unchecked
> * Deselect all software packages
> * Device for boot loader installation: /dev/XXX

## Building CrispyBox

1. Login to CrispyBox

2. Download the CrispyBox build script:
```shell
wget http://aprettycoolprogram.com/projects/crispybox/crispybox.sh
```

3. Make the script executable:
```shell
chmod +x crispybox.sh
```

The CrispyBox script automatically installs Dropbox, so if you are using another cloud-provider, you will want to change the code for that.

Also, parts of this script are interactive.

4. Run the script:
```shell
./crispybox -build
```

Once the script has completed, reboot the machine. You will then need to [initialize Dropbox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Get_official.md) (or the provider of your choice).

You may also want to convert the standard CrispyBox into a [personal CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Get_official.md), which is a bit more set-and-forget, but slightly less secure.
