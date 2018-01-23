# Building CrispyBox from scratch
If you want to use a Linux distribution other than Debian, a cloud storage provider other than Dropbox, modify any of the default settings for the Official CrispyBox, or just want to have lots and lots of fun, you'll need to build your own CrispyBox.

And in order to build your own CrispyBox, you will need:
* A working knowledge of Linux, specifically the distribution you will be using
* Virtualization software
* A Linux installer
* The instructions below
* Time

## CrispyBox requirements
If you want to build an Official CrispyBox, you will need the following:
* [Debian linux](https://www.debian.org), version 9.3.0 (we recommend that you use the [network install ISO](https://www.debian.org/CD/netinst/)).
* [Oracle VirtualBox](https://www.virtualbox.org/), version [5.2.6](http://download.virtualbox.org/virtualbox/5.2.6/)

Feel free to use another operating system and/or virtualization software, but understand that the instructions below may need to be changed.

## Creating the virtual machine definition
The minimum requirements of an Official CrispyBox is a VirtualBox VM with the following specifications:
> * 1 CPU
> * 512MB RAM
> * 16MB VRAM
> * 10GB Dynamic HDD
> * NAT networking

Please see [experimental ideas](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) for example of how these specifications can be tweaked. 
Next, you'll need to install the Operating System that CrispyBox will use. CrispyBox uses a 32-bit OS, since I can't think of any benifits to 64-bit that outweigh the smaller footprint of 32-bit. The instructions below are for Debian, using the "Expert Install" option from the "Advanced Options" menu. The usernames/passwords are for insructional purposes only, you'll want to change these for your install.
I choose the default options for everything except:> * Hostname: CrispyBox> * Root user: no> * Username/password: crispy/crispy> * Partition disk: use entire disk, create one partition, no swap partition, msdos format> * Drivers: Targeted> * Use non-free software: Yes> * Backported software: Yes> * Deselect all software packages



























## What is CrispyBox?CrispyBox is:* **"Portable"** -- 




If you're not familiar with Linux, or just want to get CrispyBox up and running, the easiest way to get started is to [download the Official CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Get_official_image.md). There are a few things you'll need to do, but for the most part all of the hard work has been done, and you'll be up and running in no time. The disadvantage to this method is that the Official CrispyBox uses the default CrispyBox image, credentials, sharepoints, etc. You can modify most of these things, but if you really want to customize CrispyBox, you should [build your own CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Build_official_image.md).If you want (or require) CrispyBox to be customized, you'll need to [build your own CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Build_official_image.md). You'll have full control over every aspect of building CrispyBox, from the operating system (if you want to use another Linux distribution), the cloud storage provider (if you don't use Dropbox), to the credentials. This method will take longer, and requires basic Linux knowledge.
