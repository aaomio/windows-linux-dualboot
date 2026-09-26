# Create a Bootable USB with Rufus

## Overview

Create a bootable Linux Mint USB installer using Rufus and the downloaded ISO image.

## 1. Download Rufus

Visit the official website:

https://rufus.ie

Download and launch Rufus.

## 2. Insert the USB Drive

Connect a USB drive with sufficient storage capacity.

**Warning:** All data on the USB drive may be erased during the process. Back up any important files first.

## 3. Configure Rufus

Select the following settings:

| Setting          | Value          |
| ---------------- | -------------- |
| Device           | USB drive      |
| Boot selection   | Linux Mint ISO |
| Partition scheme | GPT            |
| Target system    | UEFI (non CSM) |
| File system      | FAT32          |

Select the downloaded Linux Mint ISO using **SELECT**.

## 4. Create the Bootable USB

1. Click **START**.
2. If prompted, select **Write in ISO Image mode (Recommended)**.
3. Confirm the warning about erasing data.
4. Wait until Rufus displays **READY**.

## 5. Verify the USB

Confirm that Rufus has completed the process and that the USB is ready to boot.

## 6. Next Step

Continue to:

[Prepare Disk Space](Volume.md)
