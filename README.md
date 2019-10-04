<!-- GRU-Readme v3.1.0.191003 (https://github.com/APrettyCoolProgram/GRU-Readme) --------------------------------------
     GRU-README is customizable README.md template written in GitHub-flavored Markdown and HTML. The source contains
     an abundance of comments walking you through how to use each component.
---------------------------------------------------------------------------------------------------------------------->

<h2 align="center">
  CrispyBox
  <br>
  <img src="https://github.com/APrettyCoolProgram/CrispyBox/blob/master/reporesource/image/CrispyBoxLogoLarge.png" alt="CrispyBox" width="200">
  <br>
  A small, cross-platform, portable, VirtualBox Linux VM with Dropbox via SAMBA

  <br>
  <br>
</h2>
<br>

<div align="center">

  ![Status](https://img.shields.io/badge/status-maintained-green.svg)
  ![GitHub release](https://img.shields.io/github/release/aprettycoolprogram/CrispyBox?label=latest%20release)
  ![MadeFor](https://img.shields.io/badge/made_for-linux-blue.svg)
  ![MadeWith](https://img.shields.io/badge/made_with-bash-blue.svg)
  [![License](https://img.shields.io/github/license/APrettyCoolProgram/CrispyBox)](https://www.apache.org/licenses/LICENSE-2.0)

</div>

<h4 align="center">
  Current release: 19.1 (released January 2019)
</h4>

<h5 align="left">

  ### CONTENTS
  [ABOUT THIS REPOSITORY](#about-this-repository)<br>
  [FEATURES](#features)<br>
  [REQUIREMENTS](#requirments)<br>
  [GETTING STARTED](#getting-started)<br>
  [USAGE](#usage)<br>
  [DEVELOPMENT](#development)<br>
  [ADDENDUM](#addendum)

</h5>

# ABOUT THIS REPOSITORY
![GitHub last commit (branch)](https://img.shields.io/github/last-commit/aprettycoolprogram/CrispyBox/master)
![GitHub issues](https://img.shields.io/github/issues/APrettyCoolProgram/CrispyBox)
![GitHub pull requests](https://img.shields.io/github/issues-pr/aprettycoolprogram/CrispyBox)
[![GitHub contributors](https://img.shields.io/github/contributors/aprettycoolprogram/CrispyBox)](https://github.com/aprettycoolprogram/GRU-Readme/graphs/contributors/)

CrispyBox, is a a small-footprint, cross-platform, portable, official Dropbox client built on a VirtualBox Linux VM using SAMBA.

# FEATURES
* CrispyBox is **tiny**. The standard build of CrispyBox only needs 512MB RAM, and will take up the amount of space to store your Dropbox data, plus about 1GB for CrispyBox.
* CrispyBox is **cross-platform**. The standard build of CrispyBox uses Oracle's VirtualBox virtualization software, which is available for Windows, MacOS, and Linux.
* CrispyBox is **portable**, and can be run from pretty much anywhere, from your local HDD to a USB drive. The only requirement is that you'll need VirtualBox software installed on the computers you want to run CrispyBox.
* CrispyBox is **secure**. By default, CrispyBox requires your credentials to start, Dropbox data is only available when CrispyBox is running, and then is only available via a password-protected samba share.

# REQUIREMENTS
In order to use CrispyBox, you'll need:
* Oracle VirtualBox, ([version 6.0.0 recommended](https://www.virtualbox.org/wiki/Downloads))
* The [CrispyBox 19.1 VirtualBox Virtual Machine image](https://github.com/APrettyCoolProgram/CrispyBox/releases/download/19.1/CrispyBox-19.1.7z) (or, if you would like, you can also [build your own](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Building-CrispyBox-from-scratch.md))
* 512MB of RAM and a minimum of 2GBGB space to store the VM (which can expand up to 10GB, depending on use)

# GETTING STARTED
Before we continue, please verify you have met the [requirements](#requirements).

# USAGE
When you spin up your CrispyBox, the Dropbox deamon will automatically start. Follow the on-screen instructions to start syncing your data.

Once Dropbox starts syncing, you'll need to get the IP Address of the CrispyBox, so you'll know where to map. First, open a new instance of screen:

```Ctrl-A, c```

then get the IP for CrispyBox:

```$ ip addr show```

Finally, using your preferred method, map to "\\<IP_ADDRESS>\CrispyBox".

# DEVELOPMENT
The project is currently maintained by A Pretty Cool Program, and is generally updated annually.

### Contributing
If you are interested in contributing to this project, please see the [contributing guidelines](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/APrettyCoolProgramProjects/CODE_OF_CONDUCT.md).

# ADDENDUM 
### Acknowledgements
All icons are from [Icons8](www.icons8.com)

### Project resources
* [Repository](https://github.com/APrettyCoolProgram/CrispyBox)
* [Changelog](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/CHANGELOG.md)
* [Issues](https://github.com/APrettyCoolProgram/CrispyBox/issues)
* [Pull requests](https://github.com/APrettyCoolProgram/CrispyBox/pulls)
* [Project board](https://github.com/APrettyCoolProgram/CrispyBox/projects)
* [Wiki](https://github.com/APrettyCoolProgram/CrispyBox/wiki)
* [Security alerts](https://github.com/APrettyCoolProgram/CrispyBox/network/alerts)
* [Insights](https://github.com/APrettyCoolProgram/CrispyBox/pulse)
* [Code of conduct](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/CODE_OF_CONDUCT.md)
* [Contributing](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/CONTRIBUTING.md)
* [License](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/LICENSE.md)
* 
### Related projects
<div>
  <a href="https://github.com/APrettyCoolProgram/Crispy">
    <img src="https://github.com/APrettyCoolProgram/Crispy/blob/master/reporesource/image/CrispyLogoSmall.png" align="left" title="Crispy" width="100">
  </a>
  <br>
  <a href="https://github.com/APrettyCoolProgram/Crispy"><b>Crispy</b></a>
  <br>
  A collection of projects focusing on development environments and Linux
</div>
<br>

***
<div align="center">

  [![Developed by](https://img.shields.io/badge/developed%20by-A%20Pretty%20Cool%20Program-17806D.svg)](https://aprettycoolprogram.com)&nbsp;
  [![GitHub](https://img.shields.io/github/followers/aprettycoolprogram.svg?label=GitHub&style=social)](https://github.com/APrettyCoolProgram)&nbsp;
  [![Twitter](https://img.shields.io/twitter/follow/aprettycoolprog.svg?label=Twitter&style=social)](https://twitter.com/aprettycoolprog)&nbsp;
  [![Feedback](https://img.shields.io/badge/contact-info@aprettycoolprogram.com-17806D.svg)](mailto:feedback@aprettycoolprogram.com)&nbsp;
  [![Built using](https://img.shields.io/badge/README%20built%20using-GRU%20README-17806D.svg)](https://github.com/APrettyCoolProgram/GRU--Readme)&nbsp;

</div>