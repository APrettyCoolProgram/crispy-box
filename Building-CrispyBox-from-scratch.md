# Building your own CrispyBox

These are the steps/guidelines I used to create CrispyBox 19.1

### What you will need
* *The 32-bit Debian 9.6.0 netinst iso*, which you can download [here](https://cdimage.debian.org/debian-cd/current/i386/iso-cd/debian-9.6.0-i386-netinst.iso).
* *VirtualBox 6.0.0*, which you can download [here](https://www.virtualbox.org/wiki/Downloads). 

Other versions of Debian and VirtualBox will probably work, but have not been tested. Other Debian-based distributions will probably work, but may require some code modifications.

### Building the base image
1. Create VirtualBox v6.0.0 Virtual Machine. The following specifications are recommended, but you should modify them to suit your needs.
    
|                 |   |
|-----------------|---|
| CPU             | 1 |
| RAM             | 512MB |
| HDD             | Dynamic 10GB .VDI using Host I/O |
| VRAM            | 16MB | 
| 3D Acceleration | Disabled |
| Clipboard       | Disabled |

2. Install Debian 9.6.0, using "Advanced Options > Expert Install"

| Accept all defaults, except                 |   |   | 
|---------------------------------------------|---|   |
| Hostname                                    | CrispyBox |   |
| Enable Shadow Passwords                     | No |   |
| Allow login as root                         | No |   |
| Username/password                           | "crispy"/"crispy" |   | 
| Modules to load                             | usb-storage (USB storage | Unchecked |
| Partitioning method                         | Primary | 10GB msdos-formatted "/" partition |
|                                             | Logical | 700MB msdos-formatted "swap" partition |
| Kernel                                      | Targeted |   |
| Enable source repositories in APT           | No |   |
| Allow login as root                         | No |   |
| Packages to install                         | virtualbox-ose-guest-x11 | Unchecked |
| Choose software to install                  | Uncheck all options |   |
| Device for boot loader installation         | /dev/sda |   |

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

Once Dropbox starts syncing, you'll need to get the IP Address of the CrispyBox, so you'll know where to map. First, open a new instance of screen:
    ```
    Ctrl-A, c
    ```	, then get the IP for CrispyBox:
    ```
    $ ip addr show
    ```.

Finally, using your preferred method, map to "\\<IP_ADDRESS>\CrispyBox".