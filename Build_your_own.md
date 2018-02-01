# Building your own CrispyBox
You'll need to build CrispyBox yourself if want/need to:
* use a non-Debian-based Linux distribution
* use a cloud provider other than Dropbox
* have more than a maximum of 10GB (9GB for Dropbox) available for storage
* just have alot of fun!

## Building a standard CrispyBox
*These instructions will build a standard CrispyBox, version 0.9.6-beta-standard+180201*

### Requirements
The standard build of CrispyBox has the following minimum requirements:
* A Linux operating system installation ISO (32-bit Debian v9.3.0 is recommended)
* Virtualization software (Oracle VirtualBox v5.2.6 is recommended)
* A working knowledge of the Linux command line
* An internet connection
* 30-60 minutes

These instructions will need to be modified if the above recommendations are not met.

### Creating the virtual machine
The recommended specifications of an CrispyBox virtual machine are:
> * 1 CPU
> * 512MB RAM
> * 16MB VRAM
> * 10GB Dynamic HDD
> * Bridged networking

These specifications can be changed to meet your needs.

### Installing the base operating system
These instructions are for Debian, using the "Advanced options > Expert install" installation options. If you are using another operating system, try and mirror these as much as possible.

Just take the default options for each choice, except for the following:
> * USB-storage driver: unchecked
> * Hostname: CrispyBox
> * Root user: no
> * Create normal account: crispy/crispy
> * Partition disk: guided partitioning using the entire disk
> * Kernel: 686
> * Drivers: Targeted
> * Use non-free software: Yes
> * Enable source repositories: Yes
> * Backported software: checked
> * virtualbox-ose-guest-x11: unchecked
> * Deselect all software packages
> * Device for boot loader installation: /dev/XXX

### Building CrispyBox
Once you have built the virtual machine:

1. Login to CrispyBox

2. Download the CrispyBox build script:
```shell
$ wget http://aprettycoolprogram.com/projects/crispybox/crispybox.sh
```

3. Make the script executable:
```shell
$ chmod +x crispybox.sh
```

*Notes: This script is interactive, and installs the Dropbox cleint by default.*

4. Run the script:
```shell
$ ./crispybox -build
```

Once the script has completed, reboot the machine. You will then need to initialize Dropbox by following the instructions on the screen.
