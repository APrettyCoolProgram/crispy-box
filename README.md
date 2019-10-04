<!-- GRU-Readme v3.1.0.191003 (https://github.com/APrettyCoolProgram/GRU-Readme) --------------------------------------
     GRU-README is customizable README.md template written in GitHub-flavored Markdown and HTML. The source contains
     an abundance of comments walking you through how to use each component.
---------------------------------------------------------------------------------------------------------------------->

<h2 align="center">
  CrispyBox
  <br>
  <br>
  <img src="https://github.com/APrettyCoolProgram/CrispyDeven/blob/master/reporesource/image/CrispyBoxLogoLarge.png" alt="CrispyDeven" width="200">
  <br>
  <br>
  A cross-platform, portable, official Dropbox client built on a VirtualBox Linux VM 
</h2>

<div align="center">
    <img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg" alt="License">
    <img src="https://img.shields.io/badge/Platform-Linux-blue.svg" alt="Platform">
    <img src="https://img.shields.io/badge/Language-Bash-blue.svg" alt="Language">
    <img src="https://img.shields.io/badge/status-maintained-green.svg" alt="Maintained">
</div>

<h4 align="center">
  Current release: 19.1 (released January 2019)
</h4>

<h5 align="left">

  ### CONTENTS
  [FEATURES](#features)<br>
  [REQUIREMENTS](#requirments)<br>
  [BEFORE YOU BEGIN](#before-you-begin)<br>
  [INSTALLATION](#installation)<br>
  [CONFIGURATION](#configuration)<br>
  [USAGE](#usage)<br>
  [HOW IT WORKS](#how-it-works)<br>
  [FAQ](#faq)<br>
  [DEVELOPMENT](#development)<br>
  [ADDENDUM](#addendum)

</h5>

***

CrispyBox, part of the [Crispy project](https://github.com/APrettyCoolProgram/Crispy), is a a small-footprint, cross-platform, portable, official Dropbox client built on a VirtualBox Linux VM using SAMBA.

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

### Releases
CrispyBox is part of the  [Crispy](https://github.com/APrettyCoolProgram/Crispy) development cycle, although updates are quarterly rather than monthly. The current release of CrispyBox is version 19.1 (January 2019).

To ensure stability not much changes between releases. The (boring) changelog is [here](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Changelog.md).

### Using CrispyBox
When you spin up your CrispyBox, the Dropbox deamon will automatically start. Follow the on-screen instructions to start syncing your data.

Once Dropbox starts syncing, you'll need to get the IP Address of the CrispyBox, so you'll know where to map. First, open a new instance of screen:

```Ctrl-A, c```

then get the IP for CrispyBox:

```$ ip addr show```

Finally, using your preferred method, map to "\\<IP_ADDRESS>\CrispyBox". 

### Acknowledgements
All icons are from [Game Icons](http://game-icons.net).
