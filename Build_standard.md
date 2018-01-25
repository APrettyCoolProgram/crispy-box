# Building the standard build of CrispyBox
*These instructions will build a standard CrispyBox, version 0.9.5-beta+180124*

## What is the a standard CrispyBox build
A standard build of CrispyBox is a basic CrispyBox with default values.

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
> * Root user: no
> * Create normal account: crispy/crispy
> * Partition disk: use entire disk, create one partition, no swap partition, msdos format
> * Drivers: Targeted
> * Use non-free software: Yes
> * Enable source repositories: Yes
> * Backported software: Checked
> * virtualbox-ose-guest-x11: unchecked
> * Deselect all software packages
> * Device for boot loader installation: /dev/XXX

Please see [experimental ideas](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) for example of how these specifications can be tweaked. 

## Preparation
Before building a standard CrispyBox, we recommend that you read through the [experimental ideas](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) for example of how you can customize your CrispyBox build.

## Building CrispyBox
1. Login to your newly created CrispyBox as root.

2. Upgrade the system. This way we start with a nice, blank slate.
```shell
$ apt update
$ apt upgrade
```

3. Install pre-requisite packages. Use the `"-no-install-recommends" flag so recommended packages aren't installed.
```shell
$ apt install sudo ca-certificates samba screen --no-install-recommends
```

4. Give the crispy user sudo access
```shell
$ adduser crispy sudo
```

5. Create the samba credentials for crispy (password: "crispy").
```shell
$ smbpasswd -a crispy
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

7. Logout as root, then login as crispy
```shell
$exit
```

7. Install Dropbox. If you're using another cloud-based provider, skip this step.
```shell
$ wget -O - "https://www.dropbox.com/download?plat=lnx.x86" | tar xzf -
``` 

8. Cleanup.
```shell
$ sudo apt autoremove
$ sudo apt autoclean
$ sudo apt clean
$ history -cw
```
And...you've built a standard CrispyBox!

## Next steps

The standard build of CrispyBox requires you to login to start synching, and requires a password when using `sudo`. You can remove these two requirements by modifying your standard build to a [personal build](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Build_personal.md). Keep in mind that personal builds are not as secure as standard builds.

Also, remember to take a look at [experimental ideas](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) for ways to reduce the footprint of CrispyBox, add security, or other options.

Then, when you are ready, we'll [start Dropbox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Start_Dropbox_sync.md).
