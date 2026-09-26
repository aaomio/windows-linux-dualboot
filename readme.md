# Windows 11 + Linux Mint Dual Boot

A step-by-step guide to installing Linux Mint alongside Windows 11 on a UEFI/GPT system, documenting the preparation, installation, and dual-boot configuration process.

## Installation Guide

1. [Download Linux Mint](linux-download.md)
2. [Create a Bootable USB with Rufus](rufus.md)
3. [Prepare Disk Space](volume.md)
4. [Configure BIOS/UEFI](BIOS.md)
5. [Install Linux Mint](linuxinstall.md)

## Project Overview

The project documents the process of configuring a Windows 11 and Linux Mint dual-boot environment, including disk preparation, firmware settings, and bootloader configuration.

## System Configuration

* **Operating System:** Windows 11 + Linux Mint Cinnamon
* **Partition Scheme:** GPT
* **Boot Mode:** UEFI
* **Bootloader:** GNU GRUB
* **Installation Type:** Dual boot

## Notes

* Back up important data before modifying partitions or firmware settings.
* Keep the existing Windows EFI and recovery partitions intact.
* Leave Linux installation space unallocated in Windows.
* Secure Boot and storage-controller settings depend on the system configuration.
