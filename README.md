# Gentoo Linux on Pinebook
Forked from https://github.com/Linux-BSD/void-pine64
Build scripts for creating Gentoo Linux images for Pinebook laptops.

**This is currently a hack.** I'm extracting the A64/A64+ (non-LTS) kernel + uboot from pre-built Arch Linux images by [Anarsoul](https://github.com/anarsoul/linux-build/releases) and using the pre-built ROOTFS for aarch64 provided by [Gentoo Linux](https://gentoo.osuosl.org/experimental/arm64/).

It should be easy to adopt the scripts to make similar images for the Sopine module, A64/A64+ LTS boards, and the Pine64.

## Usage

Transfer the image to a micro-SD card using `dd` and boot up. 

## Build Instructions

You have to be root on the machine where you want to run these scripts as they use the `losetup` command which requires root access. You also need `wget`, `xz`, `bash`.

Use `mk-gentoo-image.sh`. The script will download Anarsoul's Arch Linux image and Gentoo Linux's ROOTFS, so you need an internet connection.

The scripts are not foolproof and will fail at first error. Depending upon where it fails you may have to do some manual clean up before being able to re-run.

## DISCLAIMER

I am not officially involved with either Pine64 or Gentoo Linux. I'm just a happy Gentoo user who wants to run it on Pine64 boards. You can cause serious damage to your equipment using these scripts and/or the images built using these scripts, and I'm not responsible if you do.
