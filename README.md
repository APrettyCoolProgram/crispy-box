<h1 align="center">
    <img src="https://github.com/APrettyCoolProgram/CrispyDeven/blob/master/AppData/Images/Project/CrispyBox-256.png" alt="CrispyDeven" width="256">
    <br>
    CrispyDeven
    <br>
    <img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg" alt="License">
    <img src="https://img.shields.io/badge/Platform-Linux--32%2F64-blue.svg" alt=".NET version">
    <img src="https://img.shields.io/badge/Development%20Status-Active-brightgreen.svg" alt="Development status">
    <a href="https://help.github.com/articles/about-pull-requests/">
        <img src="https://img.shields.io/badge/Pull Requests-Go%20for%20it-brightgreen.svg?style=shields" alt="Pull requests">
    </a>
</h1>

CrispyBox is a a small-footprint, cross-platform, portable, official Dropbox client built on a VirtualBox Linux VM using SAMBA.

### Features
* CrispyBox is **tiny**. The standard build of CrispyBox only needs 512MB RAM, and will take up the amount of space to store your Dropbox data, plus about 1GB for CrispyBox.
* CrispyBox is **cross-platform**. The standard build of CrispyBox uses Oracle's VirtualBox virtualization software, which is available for Windows, MacOS, and Linux.
* CrispyBox is **portable**, and can be run from pretty much anywhere, from your local HDD to a USB drive. The only requirement is that you'll need VirtualBox software installed on the computers you want to run CrispyBox.
* CrispyBox is **secure**. By default, CrispyBox requires your credentials to start, Dropbox data is only available when CrispyBox is running, and then is only available via a password-protected samba share.

### Requirements
In order to use CrispyBox, you'll need:
* Oracle VirtualBox, ([version 6.0.0 recommended](https://www.virtualbox.org/wiki/Downloads))
* The [CrispyBox 19.1 VirtualBox Virtual Machine image](https://github.com/APrettyCoolProgram/CrispyBox/releases/download/19.1/CrispyBox-19.1.7z) (or, if you would like, you can also [build your own](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Building-CrispyBox-from-scratch.md))
* 512MB of RAM and a minimum of 2GBGB space to store the VM (which can expand up to 10GB, depending on use)

### Using CrispyBox
When you spin up your CrispyBox, the Dropbox deamon will automatically start. Follow the on-screen instructions to start syncing your data.

Once Dropbox starts syncing, you'll need to get the IP Address of the CrispyBox, so you'll know where to map. First, open a new instance of screen:

```Ctrl-A, c```

then get the IP for CrispyBox:

```$ ip addr show```

Finally, using your preferred method, map to "\\<IP_ADDRESS>\CrispyBox". 