# Build your own Volumio x86 linux kernel
Copyright (c) 2022 Gé Koerkamp / ge.koerkamp@volum##.com

## Intro
This script is used for building the x86 kernel used for Volumio 3.  

## Prerequisites

This build process has been tested on Debia Buster (Debian 10), but should work on any Ubuntu >= 20.xy  
You will need the following minimal packages:

```
build-essential bc kmod flex cpio libncurses5-dev libelf-dev
```

## Process

### Clone the build repository

```
git clone https://github.com/gkkpch/volumio-x86-build-kernel --depth 1
```
### Run the build process

```
cd volumio-x86-build-kernel
./buildx86kernel.sh
```

### Patching


After cloning/ updating the kernel and platform repos and applying volumio patches, the build process comes to a break-point and displays:
```
[ .. ] Now ready for additional sources and patches [ Info ]
```
At this point further patches can be made in the kernel tree.  
Kernel patches are accumulated in ```./patches/volumio-kernel.patch```.  
When you're ready, or did not have any patches, press [Enter]

**Note** Currently, additional files are not automatically saved, you need to copy these into the build repo's sources folder, representing the spot in the tree where you wish to add them (create the corresponing directory tree ).


There is also an opportunity to change kernel configuration settings, using the menuconfig dialogue which will appear.
Just exit when you have no chnages.
