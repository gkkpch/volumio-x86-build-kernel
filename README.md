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
