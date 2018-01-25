# Building the standard build of CrispyBox
*These instructions will build a personal CrispyBox, version 0.9.5-beta+180124*  

## What is the a personal CrispyBox
A personal build of CrispyBox is the standard build with some security removed to make it easier to start. It's called "personal" because you should only use this build in environments that you have total control over, since once you start CrispyBox everything will just start working (although you will still need to use your CrispyBox credentials to login to the samba share).

## Requirements
* A [standard build] of CrispyBox (https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Build_standard.md)
* An internet connection
* About 5 minutes

## Removing the password requirements for `sudo`
*This is obviously a huge security risk, use with caution!*
Personally I don't want to be prompted to enter my password when using sudo, so I remove that requirement.

1. Login to CrispyBox as the crispy user

2. Start `visudo`
```shell
$ sudo visudo
```
Add the following to the bottom of the file:
```
crispy ALL=(ALL) NOPASSWD: ALL
```
3. Reboot (unless you are going to continue building a personal CrispyBox)

## Setting CrispyBox to autologin
*This is obviously a huge security risk, use with caution!*
Personally I don't want to login when CrispyBox starts, so I'll have my username login automatically.

1. Login to CrispyBox as the crispy user

2. Open the getty@.service file
```shell
$ sudo nano /lib/systemd/system/getty@.service
```
Change this line:`ExecStart=-/sbin/agetty --noclear %I $TERM" to "ExecStart=-/sbin/agetty --noclear %I $TERM`
to this:`ExecStart=-/sbin/agetty --noclear %I $TERM" to "ExecStart=-/sbin/agetty --noclear -a crispy %I $TERM`

3. Reboot (unless you are going to continue building a personal CrispyBox)

## Build complete

Congrats!
