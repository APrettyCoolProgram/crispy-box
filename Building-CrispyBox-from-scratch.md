# Building your own CrispyBox

These are the steps/guidelines I used to create CrispyBox 19.1

### What you will need
* The [32-bit Debian 9.6.0 netinst iso](https://cdimage.debian.org/debian-cd/current/i386/iso-cd/debian-9.6.0-i386-netinst.iso)
* [VirtualBox 6.0.0](https://www.virtualbox.org/wiki/Downloads)

Other versions of Debian and VirtualBox will probably work, but have not been tested. Other Debian-based distributions will probably work, but may require some code modifications.

### Building the base image
Create VirtualBox v6.0.0 Virtual Machine. The following specifications are recommended, but you should modify them to suit your needs.
    
|                 |   |
|-----------------|---|
| CPU             | 1 |
| RAM             | 512MB |
| HDD             | Dynamic 10GB .VDI using Host I/O |
| VRAM            | 16MB | 
| 3D Acceleration | Disabled |
| Clipboard       | Disabled |

Then, install Debian 9.6.0, using "Advanced Options > Expert Install"

|  Accept all defaults, except        |   |   |
|-------------------------------------|---|---|
| Hostname                            | CrispyBox |   |
| Enable Shadow Passwords             | No |   |
| Allow login as root                 | No |   |
| Username/password                   | "crispy"/"crispy" |   | 
| Modules to load                     | usb-storage (USB storage | Unchecked |
| Partitioning method                 | Primary | 10GB msdos-formatted "/" partition |
|                                     | Logical | 700MB msdos-formatted "swap" partition |
| Kernel                              | linux-image-686 |   |
| Include in the initrd               | targeted |   |
| Use non-free software               | No |   |
| Use contrib software                | No |   |
| Enable source repositories in APT   | No |   |
| Allow login as root                 | No |   |
| Packages to install                 | virtualbox-ose-guest-x11 | Unchecked |
| Choose software to install          | Uncheck all options |   |
| Device for boot loader installation | /dev/sda |   |

Once the installation is complete, the system will reboot. When the system is back up, login as "crispy/crispy", then download and execute the CrispyBox build script:

```
$ wget http://aprettycoolprogram.com/projects/CrispyBox/crispybox-build.sh
$ chmod +x crispybox-build.sh
$ ./crispybox-build.sh
```	

After the script completes, the system will shutdown.
	
Start the VM, and then follow the instructions under "Using CrispyBox" [here](https://github.com/APrettyCoolProgram/CrispyBox).
