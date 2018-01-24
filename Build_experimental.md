# Experimental build


## What is the experimental build

## Install the  localepurge package
1. Login as CrispyBox as localepurge.

2. Install the `localepurge` package (it will also run)
```
$ sudo apt localepurge
```
## Removing documentation
I'm not sure how much this will remove.
1. Login to CrispyBox as crispy

2. Remove documentation
```shell
$ sudo rm -rf /user/shared/man/*
$ sudo rm -rf /user/shared/doc/*
```

### Using bleachbit
This is the best bang for your buck. This can save 200-250MB of space. Remove after using.
1. Login to CrispyBox as root

2. Install the `bleachbit` package
```shell
$ apt install bleachbit --no-install-recommends
```
3. Run it
```
$ bleachbit --list | grep -E "[a-z]+\.[a-z]+" | xargs bleachbit --clean
```
3. Remove, we don't need it anymore
```shell
$ apt purge bleachbit
```
4. Clean
```shell
$ apt autoremove
$ apt autoclean
$ apt clean
```






