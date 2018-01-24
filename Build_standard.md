# Building the standard build of CrispyBox
*These instructions will build a standard CrispyBox, version 0.9.5-beta+180124 *  

## Requirements
The standard build of CrispyBox has the following minimum requirements:
* A Linux operating system installation ISO
* Virtualization software
* A working knowledge of the Linux command line
* An internet connection
* About 30 minutes

## Recommendations
The standard build of CrispyBox has the following recommendations:
* [Debian linux](https://www.debian.org), version 9.3.0 [network install ISO](https://www.debian.org/CD/netinst/).
* Use a 32-bit operating system, unless you have a specific need for 64-bit.
* [Oracle VirtualBox](https://www.virtualbox.org/), version [5.2.6](http://download.virtualbox.org/virtualbox/5.2.6/).

These instructions will need to be modified if the above recommendations are not met.

## Creating the virtual machine
The minimum specifications of an CrispyBox virtual machine are:
> * 1 CPU
> * 512MB RAM
> * 16MB VRAM
> * 10GB Dynamic HDD
> * Bridged networking

Please see [experimental ideas](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) for example of how these specifications can be tweaked for your environment. 

## Installing the base operating system
These instructions are for Debian, using the "Advanced options > Expert install" installation options. If you are using another operating system, try and mirror these as much as possible.

Just take the default options for each choice, except for the following:
> * USB-storage driver: unchecked
> * Hostname: CrispyBox
> * Root user: yes, root/crispy
> * Create normal account: yes, crispy/crispy
> * Partition disk: use entire disk, create one partition, no swap partition, msdos format
> * Drivers: Targeted
> * Use non-free software: Yes
> * Enable source repositories: Yes
> * Backported software: Checked
> * virtualbox-ose-guest-x11: unchecked
> * Deselect all software packages
> * Device for boot loader installation: /dev/XXX

Please see [experimental ideas](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) for example of how these specifications can be tweaked. 

## Building CrispyBox
The following steps will build a standard, CrispyBox. Before building CrispyBox, we recommend that you read through the [experimental ideas](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) for example of how you can customize your CrispyBox build.

When you are ready to build CrispyBox:
1. Login to your newly created CrispyBox as root.

2. Upgrade the system. This way we start with a nice, blank slate.
```shell
$ apt update
$ apt upgrade
```

3. Install pre-requisite packages. Use the "--no-install-recommends" flag so recommended packages aren't installed.
```shell
$ apt install sudo ca-certificates samba screen --no-install-recommends
```

4. Give the crispy user sudo access
```shell
$ adduser crispy sudo
```

5. Create the samba credentials for crispy (password: "crispy").
```shell
$ smbpasswd -a CrispyBox
``` 

6. Modify the samba configuration file.
```shell
$ nano /etc/samba/smb.conf
``` 
Add the following to the bottom of that file:
```
[CrispyBox]
path = /home/crispy
available = yes
valid users = crispy
read only = no
browsable = yes
public = yes
writable = yes
```

7. Install Dropbox. If you're using another cloud-based provider, skip this step.
```shell
$ wget -O - "https://www.dropbox.com/download?plat=lnx.x86" | tar xzf -
``` 

8. Cleanup.
```shell
$ apt autoremove
$ apt autoclean
$ apt clean
$ history -cw
```
And...you've built a standard CrispyBox!

Remember to take a look at [experimental ideas](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) for ways to reduce the footprint of CrispyBox, add security, or other options.

Then, when you are ready, we'll start the Dropbox deamon.
