# CrispyBox
My GitHub page has a bunch of nice, clean, working projects. But as a solo hobbyist programmer,the project I am working on depends on my mood and/or what intrests me at the time. That means I have alot of ugly, unfinished code that isn't ready for GitHub. For those projects, I use Dropbox as a code repository.

My Dropbox code repository contains all of my working code, both personal and professional. I don't want all of that synched with my work computers, so I don't install Dropbox on them. But then how do I access my code repository at work? Dropbox doesn't have a portable version, and the hacks that are out there are dubious at best.

So I created CrispyBox, a small-footprint virtual machine that runs the (official) Dropbox daemon to synch data that is available via a samba share.

## What is CrispyBox?
CrispyBox is:
* **"Portable"** -- I put "portable" in quotes because most likely you'll need virtualization software installed on the computers you want to run CrispyBox on (see [experimental ideas](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) for more information about getting around this requirement). But CrispyBox itself can be run from pretty much anywhere, from your local HDD to a USB drive.
* **Cross-platform** -- The official CrispyBox uses Oracle's VirtualBox virtualization software, which is available for Windows, MacOS, and Linux.
* **Secure** -- Dropbox data is only available when CrispyBox is running, and then is only available via a password-protected samba share. And here are [other ways](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) to make CrispyBox even more secure.
* **Tiny-ish** -- This really depends on how CrispyBox is built, and much data you have in Dropbox. CrispyBox itself only takes up 512MB of RAM and ~850GB of harddrive space.

## Getting started
If you're not familiar with Linux, or just want to get CrispyBox up and running, the easiest way to get started is to [download the Official CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Get_official.md). There are a few things you'll need to do, but for the most part all of the hard work has been done, and you'll be up and running in no time. The disadvantage to this method is that the Official CrispyBox uses the default CrispyBox image, credentials, sharepoints, etc. You can modify most of these things, but if you really want to customize CrispyBox, you should [build your own CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Build_official_image.md).

If you want (or require) CrispyBox to be customized, you'll need to [build your own CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Build_from_scratch.md). You'll have full control over every aspect of building CrispyBox, from the operating system (if you want to use another Linux distribution), the cloud storage provider (if you don't use Dropbox), to the credentials. This method will take longer, and requires basic Linux knowledge.

Independent of the method you choose, it is recommended that you check out the [experimental ideas](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md) for other cool things you can do with CrispyBox, how to reduce its footprint, and ways to make your data even more secure.

Have fun!
