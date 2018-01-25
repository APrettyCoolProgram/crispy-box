# CrispyBox

#### CrispyBox is a small-footprint virtual machine that runs the (official) Dropbox daemon to synch Dropbox data, which is then available via a samba share.

* CrispyBox is **portable**, and can be run from pretty much anywhere, from your local HDD to a USB drive.. You'll need virtualization software installed on the computers you want to run CrispyBox on (see [experimental ideas](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) for more information about getting around this requirement).
* CrispyBox is **cross-platform**. The standard build of CrispyBox uses Oracle's VirtualBox virtualization software, which is available for Windows, MacOS, and Linux.
* CrispyBox is **secure**. By default, CrispyBox requires your credentials to start, Dropbox data is only available when CrispyBox is running, and then is only available via a password-protected samba share. And there are [other ways](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) to make CrispyBox even more secure.
* CrispyBox is **tiny**. The standard build of CrispyBox will take up the amount of space to store your Dropbox data, plus about 1.4GB for CrispyBox. And there are [other ways](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) to reduce the footprint even farther.

## Using a pre-built CrispyBox
If you aren't very familiar with Linux, or just want to get up and running, the easiest way to get started with CrispyBox is to download a the latest pre-built CrispyBox. There are a few things you'll need to do, but for the most part all of the hard work has been done, and you'll be up and running in no time.

The standard CrispyBox build (download [here](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Build_your_own_CrispyBox.md)):
* Is built on Debian Linux
* Requires VirtualBox (recommended version 5.2.6)
* Uses Dropbox
* Has a 9GB virtual HDD for Dropbox storage
* Requires at least 1GB of local HDD space, and up to 10GB local HDD space (depending on the amount of Dropbox data)
* Requires login to start
* Requires password for sudo access
* Requires authentication for fileshare

The personal CrispyBox build (download [here](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Build_your_own_CrispyBox.md)) is the same as the standard build, except:
* Is set to autologin
* Does not require a password for sudo access

## Building your own CrispyBox
[Building your own CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Build_your_own_CrispyBox.md) is the best way to customize CrispyBox to your needs. You'll have full control over every aspect of building CrispyBox, from the operating system (if you want to use another Linux distribution), the cloud storage provider (if you don't use Dropbox), to the credentials. This method will take longer, and requires basic Linux knowledge.

Have fun!
