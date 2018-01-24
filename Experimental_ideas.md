# Experimental ideas
This is a list of things you can do to reduce the CrispyBox footprint, increase security, and add functionality.

## Reducing the CrispyBox footprint
*These instructions are all experimental! Use at your own risk!*
While CrispyBox isn't large (the standard image is approximately 1GB), I'm certian that there is alot of reduction that can be done.

### Using localepurge
1. Login as CrispyBox as localepurge.

2. Install the `localepurge` package (it will also run)
```
$ sudo apt localepurge
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

### Using deborphan
I'm not sure how much this will remove.
1. Login to CrispyBox as crispy

2. Install the `deborphan` package
```shell
$ apt install deborpahn --no-install-recommends
```
3. Run it
```
$ deborphan
```

4. A list of packages that can be removed will be displayed. Remove them.

5. Remove, we don't need it anymore
```shell
$ apt purge bleachbit
```
6. Clean
```shell
$ apt autoremove
$ apt autoclean
$ apt clean
```


