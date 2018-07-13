# CrispyBox
A a small-footprint, cross-platform, portable, official Dropbox client built on a VirtualBox Linux VM using SAMBA.

* CrispyBox is **tiny**. The standard build of CrispyBox only needs 512MB RAM, and will take up the amount of space to store your Dropbox data, plus about 1GB for CrispyBox.
* CrispyBox is **cross-platform**. The standard build of CrispyBox uses Oracle's VirtualBox virtualization software, which is available for Windows, MacOS, and Linux.
* CrispyBox is **portable**, and can be run from pretty much anywhere, from your local HDD to a USB drive. The only requirement is that you'll need VirtualBox software installed on the computers you want to run CrispyBox.
* CrispyBox is **secure**. By default, CrispyBox requires your credentials to start, Dropbox data is only available when CrispyBox is running, and then is only available via a password-protected samba share.


The stable version of CrispyBox is released quarterly. The current version is Summer18. Please see the [changelog](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Changelog.md)<br> for the version history.

The CrispyBox Summer18 release is built on 32-bit Debian 9.4, and includes:
* ca-certificates
* Dropbox deamon
* samba 
* screen

In order to use CrispyBox, you'll need:
* Oracle VirtualBox (version 5.2.14 recommended)
* A CrispyBox VirtualBox Virtual Machine
* 512MB of RAM
* A minimum of 2GBGB space to store the VM (which can expand up to 10GB, depending on use).

I recommend you download the [pre-built](http://aprettycoolprogram.com/projects/CrispyBox/CrispyBox-Summer18.7z) Summer18 release, which is a VirtualBox 5.2.14 Virtual Machine with the following specifications:
* CPU: 1
* RAM: 512MB
* HDD: Dynamic 100GB .VDI using Host I/O
* VRAM: 16MB
* 3D Acceleration: Disabled
* Clipboard: Disabled

If you require different specifications for your CrispyDeven Virtual Machine, you can [build your own](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Building-CrispyBox-from-scratch.md) CrispyBox from scratch.

When you spin up your CrispyBox, the Dropbox deamon will automatically starts. Follow the on-screen instructions to start syncing your data.

Once Dropbox starts syncing, you'll need to get the IP Address of the CrispyBox, so you'll know where to map. First, open a new instance of screen:
    ```
    Ctrl-A, c
    ```	, then get the IP for CrispyBox:
    ```
    $ ip addr show
    ```.

Finally, using your preferred method, map to "\\<IP_ADDRESS>\CrispyBox".