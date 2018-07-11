# CrispyBox

***NOTE***: CrispyBox is being rolled into CrispyDev. I'm leaving this code here for historical purposes.

#### CrispyBox is a small-footprint virtual machine that runs the (official) Dropbox daemon to synch Dropbox data, which is then available via a samba share.

* CrispyBox is **portable**, and can be run from pretty much anywhere, from your local HDD to a USB drive. The only requirement is that you'll need virtualization software installed on the computers you want to run CrispyBox.
* CrispyBox is **cross-platform**. The standard build of CrispyBox uses Oracle's VirtualBox virtualization software, which is available for Windows, MacOS, and Linux.
* CrispyBox is **secure**. By default, CrispyBox requires your credentials to start, Dropbox data is only available when CrispyBox is running, and then is only available via a password-protected samba share.
* CrispyBox is **tiny**. The standard build of CrispyBox will take up the amount of space to store your Dropbox data, plus about 1GB for CrispyBox.

## Using a pre-built CrispyBox
If you aren't very familiar with Linux, or just want to get up and running, the easiest way to get started with CrispyBox is to download a the latest [pre-built CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Pre-built_images.md). There are a few things you'll need to do, but for the most part all of the hard work has been done, and you'll be up and running in no time.

## Building your own CrispyBox
[Building your own CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Build_your_own.md) is the best way to customize CrispyBox to your needs. You'll have full control over every aspect of building CrispyBox, from the operating system (if you want to use another Linux distribution), the cloud storage provider (if you don't use Dropbox), to the credentials. This method will take longer, and requires basic Linux knowledge.

Have fun!
