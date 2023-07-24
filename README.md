# Buildroot Package for Miyoo CFW 2.0.0
Opensource development package for Miyoo handhelds

## Install

### Install necessary packages
``` shell
sudo apt install -y wget unzip build-essential git bc swig libncurses-dev libpython3-dev libssl-dev cpio rsync subversion python3
```

### Download BSP
```shell
git clone https://github.com/MiyooCFW/buildroot
```

## Make the first build

### Apply defconfig uClibc

```shell
cd buildroot
make miyoo_uclibc_defconfig
```

### Or apply defconfig musl

```shell
cd buildroot
make miyoo_musl_defconfig
```

### Regular build
```shell
make
```

## Speed up build progress

### Compile speed
If you have a multicore CPU, you can try
```
make -j ${YOUR_CPU_COUNT}
```
or buy a powerful PC for yourself.

## Flashing firmware to target

load output/images/miyoo-cfw-*.img on sdcard

## First booting device
You will have to answer a few questions on first boot, represented on graphic below:
![248453556-d8952ab9-2487-49e0-8342-8a1e5cdd76a8 drawio](https://github.com/MiyooCFW/buildroot/assets/94932128/2cc32fcd-64bd-46a9-a3bb-4b72f4080204)

---
# _Buildroot 2022.02.9 (docs: https://github.com/MiyooCFW/buildroot/blob/master/docs/manual/manual.pdf)_
---
