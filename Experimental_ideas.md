
> * 1 CPU> * 512MB RAM> * 16MB VRAM> * 10GB Dynamic HDD> * NAT networking

You may be able to reduce the RAM to 256 (not tested!), and you may see better performance with a fixed HDD (not tested!).

deborphan package

> * 1 CPU> * 512MB RAM> * 16MB VRAM> * 10GB Dynamic HDD> * NAT networking
You may be able to reduce the RAM to 256 (not tested!), and you may see better performance with a fixed HDD (not tested!).

A few things to note about the build:* The username/password is "crispy/crispy". This is for ease-of-use, but is not secure (obv). Feel free to modify this, but understand that other parts of this documentation will need to change as well.* CrispyBox doesn't have a swap partition. I'm doing this to reduce the footprint, but I'm not sure how this will work out in the long-term, so you may want to include one. * I'm using a dynamic disk. You may see performance increases using a fixed disk.* If you use a dynamic disk, and want the option to compress the .vdi using the VBoxManage utility, you'll need to format the HDD as "msdos". 

Need to do as su
6. [OPTIONAL] Install the bleachbit package. If you are really going for a small footprint, you can install bleachbit. The default version of CrispyBox doesn't do this, but you could potentially remove ~150MB of unecessary stuff using bleachbit. *Again, this isn't tested, so use at your own risk!*```
```shell$ apt install bleachbit --no-install-recommends
Personally I don't want to be prompted to enter my password when using sudo, so I remove that requirement. *This is obviously a huge security risk, use with caution!*This mofication must be done using visudo...```shell  $ visudo```  ...and by adding the following to the bottom of the file..```CrispyBox ALL=(ALL) NOPASSWD: ALL```Personally I don't want to login when CrispyBox starts, so I'll have my username login automatically. *This is obviously a huge security risk, use with caution!* Open the getty@.service file...```shell   $ nano /lib/systemd/system/getty@.service```...and change this line...```ExecStart=-/sbin/agetty --noclear %I $TERM" to "ExecStart=-/sbin/agetty --noclear %I $TERM```...to this...```ExecStart=-/sbin/agetty --noclear %I $TERM" to "ExecStart=-/sbin/agetty --noclear -a CrispyBox %I $TERM```
You'll notice that I've shared out my entire "/home/CrispyBox/" path. If you want to specifiy a specific directory for sharing, therby leaving the other directories in your home folder inaccessible, you can do so by changing this line...```path = /home/CrispyBox```...to this...```path = /home/CrispyBox/coderepository``` Finally, some cleanup. If you installed bleachbit:```shell$ bleachbit --list | grep -E "[a-z]+\.[a-z]+" | xargs bleachbit --clean```
Once CrispyBox is installed, I don't see a need to keep bleachbit around (if you do, don't do this):```shell$ apt purge bleachbit```  
If you are using a dynamic HDD, and have the option to defragment/compress the image in your virtualization software, you may want to defragment and wipe the VMs freespace:```shell$ sudo e4defrag /$ cat /dev/zero > zero.file$ sync$ rm zero.file ```
If you are using VirtualBox dynamic HDD, you may want to compact the .vdi (Other virtualization software most likely has a similar option).```C:\Program Files\Oracle\VirtualBox>VBoxManage.exe modifyhd --compact "<LOCATION-OF-CRISPY.VDI"  ```This virtual machine was created using "NAT Networking", but for the samba share to work correctly, you'll need to change to "Bridged Networking". You'll need to find where to change this setting in your virtualization software.

7. [OPTONAL] Create the .CrispyBox directory. We can put CrispyBox-related stuff here.```shell$ mkdir .CrispyBox```
8. [OPTONAL] I like to put a little history file on the system, so I know what version this is:```shell$ touch .CrispyBox/v0.9.5-beta+180123```5. [OPTIONAL] Install the htop package. It's small and helpful, but also optional.```shell$ apt install htop --no-install-recommends```
2. [OPTIONAL] Install the localepurge package. I like to install this to safely reduce the footprint of CrispyBox by removing uncecessary languages. If you need/want multiple language support, skip this step. This install is interactive, just accept the default choices.```shell$ apt install localepurge```
9. [OPTONAL] Remove manpages/documentation. I don't really see a need for manpages/documentation in CrispyBox, so I get rid of them:```shell$ rm -rf /usr/share/man/*$ rm -rf /usr/share/doc/*```
Since CrispyBox is 32-bit, we'll install the 32-bit version of Dropbox:```shell$ wget -O - "https://www.dropbox.com/download?plat=lnx.x86" | tar xzf -``` If you built CrispyBox on a 64-bit platform:```shell$ wget -O - "https://www.dropbox.com/download?plat=lnx.x86_64" | tar xzf -```
If you built CrispyBox on a 64-bit platform:```shell$ wget -O - "https://www.dropbox.com/download?plat=lnx.x86_64" | tar xzf -```
script that builds a standard CrispyBox
