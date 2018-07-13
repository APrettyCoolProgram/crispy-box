# Building your own CrispyBox (Summer18 release)

These are the steps/guidelines I used to create the Summer18 release of CrispyBox.

### What you will need
* *The 32-bit Debian 9.4.0 netinst iso*, which you can download here.
* *VirtualBox 5.2.14*, which you can download here. 

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
		> Hostname: CrispyBox
		> Enable Shadow Passwords: No
		> Allow login as root: No
		> Username/password: crispy/crispy
		> Modules to load - usb-storage (USB storage): Unchecked
		> Partitioning method - Manual
			>> 10GB msdos-formmated / partition
			>> 700MB ms-dos-formatted swap partition
		> Kernel: Targeted
		> Enable source repositories in APT: No
		> Packages to install - virtualbox-ose-guest-x11: Unchecked
		> Choose software to install: Uncheck all options
		> Device for boot loader installation: /dev/sda

3. Once the installation is complete, the system will reboot.

4. When the system is back up, login as "crispy/crispy".

5. Download and execute the CrispyDeven preparation script:
```
$ wget http://aprettycoolprogram.com/projects/CrispyDeven/crispydeven-prepare.sh
$ chmod +x crispydeven-prepare.sh
$ ./crispydeven-prepare.sh
```	
6. Once the prepration script completes, the system will reboot.
	
7. When the system is back up, login as "crispy/crispy".

8. Download and execute the CrispyDeven build script:
```
$ wget http://aprettycoolprogram.com/projects/CrispyDeven/crispydeven-build.sh
$ chmod +x crispydeven-build.sh
$ ./crispydeven-build.sh
```
9. Once the build script completes, the system will reboot.

You should now have a working CrispyDeven environment!

### Installing the VirtualBox Guest Additions
I recommend you install the VirtualBox Guest Additions, which improve performance of the CrispyDeven Virtual Machine, as well as enable useful functionality such as shared clipboards and host file access.

It's important to note that this script installs the VirtualBox Guest Additions v5.2.14. If you are using a different verison of VirtualBox, you will need to modify the code to reflect the version you are using. 
```
$ wget http://aprettycoolprogram.com/projects/CrispyDeven/crispydeven-install-vbox-guest-additions.sh
$ chmod +x crispydeven-build.sh
$ ./crispydeven-build.sh
```





### Enabling autologin
**This is significant security risk**
If you want the crispy user autologin:
```
$ sudo nano /lib/systemd/system/getty@.service
```
Then, add change this line:
```
ExecStart=-/sbin/agetty --noclear %I $TERM
```
to this:
```
ExecStart=-/sbin/agetty --noclear -a crispy %I $TERM
```

### Removing the sudo password requirements.
**This is significant security risk**
If you want to remove the password requirements when using sudo:
```
$ sudo visudo
```
Then, add this line to the bottom of the file:
```
crispy ALL=(ALL) NOPASSWD: ALL
```

