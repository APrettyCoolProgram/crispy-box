<!---------------------------------------------------------------------------------------------------------------------
FILENAME: README.md
 PROJECT: a-repository-template(https://github.com/aprettycoolprogram/gru-readme-template)
 VERSION: Version 3.3.1.191223
 UPDATED: 12-23-2019 (11:20 AM)
 AUTHORS: development@aprettycoolprogram.com

Copyright 2019 A Pretty Cool Program

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with
the License. You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0.

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on
an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the
specific language governing permissions and limitations under the License.
---------------------------------------------------------------------------------------------------------------------->

<h2 align="center">
  CrispyBox
  <br>
  <img src="https://github.com/aprettycoolprogram/crispybox/blob/master/repository-resource/image/logo/crispybox-logo-100,100.png" alt="CrispyBox" width="100">
  <br>
  A small, cross-platform, portable, VirtualBox Linux VM with Dropbox via SAMBA
  <br>
  <br>
</h2>
<br>

<div align="center">

  ![Status](https://img.shields.io/badge/status-active-brightgreen.svg)
  [![License](https://img.shields.io/github/license/aprettycoolprogram/gru-repository-template)](https://www.apache.org/licenses/LICENSE-2.0)
  ![GitHub release](https://img.shields.io/github/release/aprettycoolprogram/gru-repository-template?label=latest%20release)

</div>

<h5 align="left">

  ### CONTENTS
  [ABOUT THIS REPOSITORY](#about-this-repository)<br>
  [FEATURES](#features)<br>
  [REQUIREMENTS](#requirements)<br>
  [BEFORE YOU BEGIN](#before-you-begin)<br>
  [GETTING STARTED](#getting-started)<br>
  [INSTALLING](#installing)<br>
  [BUILD PROCESS](#build-process)<br>
  [SETUP](#setup)<br>
  [CONFIGURATION](#configuration)<br>
  [USAGE](#usage)<br>
  [UPDATING](#updating)<br>
  [UNINSTALLING](#uninstalling)<br>
  [DEMO](#demo)<br>
  [HOW IT WORKS](#how-it-works)<br>
  [API](#api)<br>
  [FAQ](#faq)<br>
  [SUPPORT](#support)<br>
  [DEVELOPMENT](#development)<br>

</h5>

# ABOUT THIS REPOSITORY
CrispyBox, is a small-footprint, cross-platform, portable, official Dropbox client built on a VirtualBox Linux VM using SAMBA.

CrispyBox is updated at the beginning of every year. After that, all updates are done from within the VM.

# FEATURES
* CrispyBox is **tiny**. The standard build of CrispyBox only needs 512MB RAM, and will take up the amount of space to store your Dropbox data, plus about 1GB for CrispyBox itself.
* CrispyBox is **cross-platform**. The standard build of CrispyBox uses Oracle's VirtualBox virtualization software, which is available for Windows, MacOS, and Linux.
* CrispyBox is **portable**, and can be run from pretty much anywhere, from your local HDD to a USB drive. The only requirement is that you'll need VirtualBox software installed on the computers you want to run CrispyBox.
* CrispyBox is **secure**. By default, CrispyBox requires your credentials to start, Dropbox data is only available when CrispyBox is running, and then is only available via a password-protected samba share.

# REQUIREMENTS
In order to use CrispyBox, you'll need:
* Oracle VirtualBox, ([version 6.1.0 recommended](https://www.virtualbox.org/wiki/Downloads))
* The [CrispyBox 20.0 VirtualBox Virtual Machine image](https://github.com/APrettyCoolProgram/CrispyBox/releases/download/19.1/CrispyBox-19.1.7z) (or, if you would like, you can also [build your own](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Building-CrispyBox-from-scratch.md))
* 512MB of RAM and a minimum of 2GBGB space to store the VM (which may increase, depending on use)

# EXAMPLES
Some examples of gru-repository-template in action:
* Example #1
* Example #2
* Example #3

# BEFORE YOU BEGIN
CrispyBox is updated once a year in January, using the latest versions of VirtualBox and Debian.

### RELATED PROJECTS
* [**Crispy**](https://github.com/APrettyCoolProgram/crispy)

# GETTING STARTED
Before we continue, please verify you have met the [requirements](#requirements).

### PRE-REQUISITES
Pre-requisites are different than requirements. Requirements are what you will need in order to use the project in any capacity (i.e. a text editor), and pre-requisites are what you need once you've met the requirements and have decided to use the project (i.e. a copy of this template file).

### DEPENDENCIES
List any dependencies, and instructions to install them, here.

### RECOMMENDATIONS
Remember: you never get a second chance to make a first impression. Put aside the necessary amount of time to create a document that is accurate, grammatically correct, and informative. Don't rush this!

<!-- INSTALLATION [Optional] ------------------------------------------------------------------------------------------
Steps to install this project.
----------------------------------------------------------------------------- (Remove this comment block when done) -->
# INSTALLING
Overview of the installation process

### WINDOWS
1. The steps to install the project in Windows
2. Use both Markdown and/or HTML
3. Include screenshots when possible.
4. Remove this section if the project doesn't support Windows (and mention that in the "Other operating systems" section below).

### MACOS
1. The steps to install the project in MacOS
2. Use both Markdown and/or HTML
3. Include screenshots when possible.
4. Remove this section if the project doesn't support MacOS (and mention that in the "Other operating systems" section below).

### LINUX
1. The steps to install the project in Linux
2. Use both Markdown and/or HTML
3. Include screenshots when possible.
4. Remove this section if the project doesn't support Linux (and mention that in the "Other operating systems" section below).

### OTHER OPERATING SYSTEMS
1. The steps to install the project in other operating systems
2. Use both Markdown and/or HTML
3. Include screenshots when possible.
4. If other operating systems are not supported, mention that here.

<!-- BUILD PROCESS [Optional] -----------------------------------------------------------------------------------------
Build process instructions.
----------------------------------------------------------------------------- (Remove this comment block when done) -->
# BUILD PROCESS
If your project has a build process, document it here.

<!-- SETUP [Optional] -------------------------------------------------------------------------------------------------
Instructions to setup your project.
----------------------------------------------------------------------------- (Remove this comment block when done) -->
# SETUP
If your project has a setup procedure, document it here. For example, you may need to make changes to a configuration
file before using the project.

<!-- CONFIGURATION [Optional] -----------------------------------------------------------------------------------------
Describe how to configure the project.
----------------------------------------------------------------------------- (Remove this comment block when done) -->
# CONFIGURATION
Many projects offer configuration options, which should be listed here. Keep in mind that any configuration that needs to be done before using this project should be listed in the [setup](#setup) section above.

### Important notes about the configuration
Optional notes about configuration go here.

<!-- USAGE [Optional] -------------------------------------------------------------------------------------------------
How to use the project.
----------------------------------------------------------------------------- (Remove this comment block when done) -->
# USAGE
This template file is filled with comments like this:
```
<!-- ABOUT THIS REPOSITORY [Required] -----------------------------------------------------------------
Introduce your repository, and encourage the reader to continue reading. You should:
* Describe what the repository is.
* What problem(s) does it solve?
* What is the motivation/philosophy behind it?
* Why should the user care or want to use it?
* List one or two noteworthy features that stand out from similar repositories
* Clarify the level of knowledge required, and note key technical concepts/technologies/frameworks used
* Use screenshots and code snippets to illustrate general functionality
* Use Markdown to make text stand out.
------------------------------------------------------------- (Remove this comment block when done) -->
```
These comments are intended to walk you through creating content for each component, and can be removed to keep your final README.md clean. Some components are [Required], and some are [Optional], but in reality these are just guidelines.

### IMPORTANT NOTES ABOUT USAGE
Optional notes about usage go here.

<!-- UPDATING [Optional] ----------------------------------------------------------------------------------------------
Updating procedure.
----------------------------------------------------------------------------- (Remove this comment block when done) -->
# UPDATING
Any updating procedures should be documented here.

<!-- UNINSTALL [Optional]----------------------------------------------------------------------------------------------
Uninstall procedure.
----------------------------------------------------------------------------- (Remove this comment block when done) -->
# UNINSTALLING
Any uninstall procedures should be documented here.

<!-- API [Optional] ---------------------------------------------------------------------------------------------------
API documentation.
----------------------------------------------------------------------------- (Remove this comment block when done) -->
# API
If your project contains an API, it should be documented here.

<!-- HOW IT WORKS [Optional] ------------------------------------------------------------------------------------------
Sometimes it's fun to let users know how the magic happens.
----------------------------------------------------------------------------- (Remove this comment block when done) -->
# HOW IT WORKS
Sometimes it's fun to let users know how the magic happens.

<!-- FAQ [Optional] ---------------------------------------------------------------------------------------------------
Frequently Asked Questions.
----------------------------------------------------------------------------- (Remove this comment block when done) -->
# FAQ
### Are you nice?
I think so.

<!-- SUPPORT [Optional] -----------------------------------------------------------------------------------------------
Support information.
----------------------------------------------------------------------------- (Remove this comment block when done) -->
# SUPPORT
Good luck!

<!-- DEVELOPMENT [Optional] -------------------------------------------------------------------------------------------
Development information.
----------------------------------------------------------------------------- (Remove this comment block when done) -->
# DEVELOPMENT
This project is currently being developed by [A Pretty Cool Program](https://github.com/APrettyCoolProgram). You can view the version history [here](documentation/changelog.md).

If your interested in what's coming in the next release, the development branch of the project can be found [development branch](https://github.com/aprettycoolprogram/a-repository-template/tree/development). You can also read the [development notes](documentation/development-notes.md).

### CONTRIBUTING
If you are interested in contributing to this project, please review our [code of conduct](documentation/code-of-conduct.md), [contributing guidelines](documentation/code-of-conduct.md), and [testing procedures](documentation/testing.md) documentation.

<!-- DEVELOPER INFORMATION [Required] ---------------------------------------------------------------------------------
Developer information.
----------------------------------------------------------------------------- (Remove this comment block when done) -->
***

<div align="center">

  [![Developed by](https://img.shields.io/badge/developed%20by-A%20Pretty%20Cool%20Program-17806D.svg)](https://aprettycoolprogram.com)&nbsp;
  [![GitHub](https://img.shields.io/github/followers/aprettycoolprogram.svg?label=GitHub&style=social)](https://github.com/aprettycoolprogram)&nbsp;
  [![Twitter](https://img.shields.io/twitter/follow/aprettycoolprog.svg?label=Twitter&style=social)](https://twitter.com/aprettycoolprog)&nbsp;
  [![Feedback](https://img.shields.io/badge/contact-info@aprettycoolprogram.com-17806D.svg)](mailto:feedback@aprettycoolprogram.com)&nbsp;
  [![Built using](https://img.shields.io/badge/built%20using-a--repository--template-17806D.svg)](https://github.com/aprettycoolprogram/a-repository-template/)&nbsp;

</div>