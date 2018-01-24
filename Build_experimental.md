# Building the experimental build of CrispyBox
*These instructions will build an experimental CrispyBox, version 0.9.5-beta+180124*

## What is an experimental CrispyBox build
An experimental build of CrispyBox is a personal CrispyBox with with some experimental features that:
* Reduce the footprint

## Building experimental
1. Login as CrispyBox as crispy.

2. Install the `localepurge` package (it will also run)
```
$ sudo apt localepurge
```

3. Remove documentation
```shell
$ sudo rm -rf /user/shared/man/*
$ sudo rm -rf /user/shared/doc/*
```

4. Login as su
```shell
$ su
```

5. Install the `bleachbit` package
```shell
$ apt install bleachbit --no-install-recommends
```
6. Run it
```
$ bleachbit --list | grep -E "[a-z]+\.[a-z]+" | xargs bleachbit --clean
```
7. Remove, we don't need it anymore
```shell
$ apt purge bleachbit
```

8. Clean
```shell
$ apt autoremove
$ apt autoclean
$ apt clean
```

## Complete
[experimental ideas](https://github.com/APrettyCoolProgram/CrispyBox/blob/master/Experimental_ideas.md)





