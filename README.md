# CrispyBox
A a small-footprint, cross-platform, portable, official Dropbox client built on a VirtualBox Linux VM using SAMBA.

* CrispyBox is **tiny**. The standard build of CrispyBox only needs 512MB RAM, and will take up the amount of space to store your Dropbox data, plus about 1GB for CrispyBox.
* CrispyBox is **cross-platform**. The standard build of CrispyBox uses Oracle's VirtualBox virtualization software, which is available for Windows, MacOS, and Linux.
* CrispyBoxnywhere, from your local HDD to a USB drive. The only requirement is that you'll need VirtualBox software installed on th is **portable**, and can be run from pretty much ae computers you want to run CrispyBox.
* CrispyBox is **secure**. By default, CrispyBox requires your credentials to start, Dropbox data is only available when CrispyBox is running, and then is only available via a password-protected samba share.

### Requirements
In order to use CrispyBox, you'll need:
* Oracle VirtualBox, ([version 6.0.0 recommended](https://www.virtualbox.org/wiki/Downloads))
* The [CrispyBox 19.1 VirtualBox Virtual Machine image](here) (or, if you would like, you can also [build your own](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Building-CrispyBox-from-scratch.md))
* 512MB of RAM and a minimum of 2GBGB space to store the VM (which can expand up to 10GB, depending on use)

## Using CrispyBox
When you spin up your CrispyBox, the Dropbox deamon will automatically start. Follow the on-screen instructions to start syncing your data.

Once Dropbox starts syncing, you'll need to get the IP Address of the CrispyBox, so you'll know where to map. First, open a new instance of screen:

```Ctrl-A, c```

then get the IP for CrispyBox:

```$ ip addr show```

Finally, using your preferred method, map to "\\<IP_ADDRESS>\CrispyBox". 