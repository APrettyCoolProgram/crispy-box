# Getting the Official CrispyBox
Downloading the latest Official CrispyBox is the easiest way to 

My Dropbox code repository contains all of my working code, both personal and professional. I don't want all of that synched with my work computers, so I don't install Dropbox on them. But then how do I access my code repository at work? Dropbox doesn't have a portable version, and the hacks that are out there are dubious at best.

So I created CrispyBox, a small-footprint virtual machine that runs the (official) Dropbox daemon to synch data that is available via a samba share.

## What is CrispyBox?
CrispyBox is:
* **"Portable"** -- 



If you're not familiar with Linux, or just want to get CrispyBox up and running, the easiest way to get started is to [download the Official CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Get_official_image.md). There are a few things you'll need to do, but for the most part all of the hard work has been done, and you'll be up and running in no time. The disadvantage to this method is that the Official CrispyBox uses the default CrispyBox image, credentials, sharepoints, etc. You can modify most of these things, but if you really want to customize CrispyBox, you should [build your own CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Build_official_image.md).
If you want (or require) CrispyBox to be customized, you'll need to [build your own CrispyBox](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Build_official_image.md). You'll have full control over every aspect of building CrispyBox, from the operating system (if you want to use another Linux distribution), the cloud storage provider (if you don't use Dropbox), to the credentials. This method will take longer, and requires basic Linux knowledge.