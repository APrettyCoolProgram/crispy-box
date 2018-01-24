# CrispyBox

#### CrispyBox is a small-footprint virtual machine that runs the (official) Dropbox daemon to synch Dropbox data, which is then available via a samba share.
---
CrispyBox is **portable**, and can be run from pretty much anywhere, from your local HDD to a USB drive.. You'll need virtualization software installed on the computers you want to run CrispyBox on (see [experimental ideas](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) for more information about getting around this requirement).

CrispyBox is **Cross-platform**. The standard build of CrispyBox uses Oracle's VirtualBox virtualization software, which is available for Windows, MacOS, and Linux.

CrispyBox is **Secure**. By default, CrispyBox requires your credentials to start, Dropbox data is only available when CrispyBox is running, and then is only available via a password-protected samba share. And there are [other ways](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) to make CrispyBox even more secure.

CrispyBox is pretty **Tiny**. The standard build of CrispyBox will take up the amount of space to store your Dropbox data, plus about 1.4GB for CrispyBox. And there are [other ways](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) to reduce the footprint even farther.

## Getting started
The easiest way to get started with CrispyBox is to download a [pre-built CrispyBox image](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Get_pre-built.md). This is the way to go if you aren't very familiar with Linux, or just want to get up and running. There are a few things you'll need to do, but for the most part all of the hard work has been done, and you'll be up and running in no time. The disadvantage to this method is that the standard build uses the default CrispyBox image, credentials, sharepoints, etc, so it's not very secure. You can modify most of these things, but if you really want to customize CrispyBox, you should [build your own CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Build_your_own_CrispyBox.md).

[Building your own CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Build_your_own_CrispyBox.md) is the best way to customize CrispyBox to your needs. You'll have full control over every aspect of building CrispyBox, from the operating system (if you want to use another Linux distribution), the cloud storage provider (if you don't use Dropbox), to the credentials. This method will take longer, and requires basic Linux knowledge.

Independent of the method you choose, it is recommended that you check out the [experimental ideas](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) for other cool things you can do with CrispyBox, how to reduce its footprint, and ways to make your data even more secure.

Have fun!
