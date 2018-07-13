# Building your own CrispyBox (Summer18 release)

These are the steps/guidelines I used to create the Summer18 release of CrispyBox.

### What you will need
* *The 32-bit Debian 9.4.0 netinst iso*, which you can download [here](https://cdimage.debian.org/debian-cd/9.4.0/i386/iso-cd/).
* *VirtualBox 5.2.14*, which you can download [here](https://www.virtualbox.org/wiki/Download_Old_Builds_5_2). 

Other versions of Debian and VirtualBox will probably work, but have not been tested. Other Debian-based distributions will probably work, but may require some code modifications.

### Building the base image
1. Create VirtualBox v5.2.14 Virtual Machine. The following specifications are recommended, but you should modify them to suit your needs.
* CPU: 1
* RAM: 512MB
* HDD: Dynamic 10GB .VDI using Host I/O
* VRAM: 16MB
* 3D Acceleration: Disabled
* Clipboard: Disabled
	
2. Install Debian 9.4.0
* Use "Advanced Options > Expert Install"
* Accept all defaults, except:
  * Hostname: CrispyBox
  * Enable Shadow Passwords: No
  * Allow login as root: No
  * Username/password: crispy/crispy
  * Modules to load - usb-storage (USB storage): Unchecked
  * Partitioning method - Manual
    * 10GB msdos-formatted / partition
    * 700MB ms-dos-formatted swap partition)
  * Kernel: Targeted
  * Enable source repositories in APT: No
  * Packages to install - virtualbox-ose-guest-x11: Unchecked
  * Choose software to install: Uncheck all options
  * Device for boot loader installation: /dev/sda

3. Once the installation is complete, the system will reboot.

4. When the system is back up, login as "crispy/crispy".

5. Download and execute the CrispyBox build script:
```
$ wget http://aprettycoolprogram.com/projects/CrispyBox/crispybox-build.sh
$ chmod +x crispybox-build.sh
$ ./crispybox-build.sh
```	
6. Once the prepration script completes, the system will reboot.
	
7. When the system is back up, login as "crispy/crispy".

Dropbox will automatically start. Follow the on-screen instructions to complete the setup.