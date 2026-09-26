# Volume.md

# Prepare Disk Space for Linux Mint

This guide covers shrinking the Windows 11 partition to create unallocated space for Linux Mint.

## 1. Open Disk Management

1. Press `Win + R`.
2. Open **Diskmgmt.msc**.
3. Locate the physical disk containing Windows 11.
4. Identify the Windows `C:` partition and check the available free space.

> **Important:** Back up important files before modifying partitions. Confirm the correct physical disk and never delete the EFI System, Windows, or recovery partitions.

## 2. Shrink the Windows Partition

1. Right-click the Windows `C:` partition.
2. Select **Shrink Volume**.
3. Wait for Windows to calculate the available shrink space.
4. Enter the amount of space to shrink in MB.

| Linux space | Amount to enter |
| ----------- | --------------: |
| 32 GB       |        32768 MB |
| 64 GB       |        65536 MB |

5. Click **Shrink**.
6. Confirm that the new space appears as **Unallocated**.

> Windows may restrict the available shrink space because of immovable files. If the available amount is smaller than the requested size, do not force the operation. Use the available space or investigate the limitation first.

## 3. Leave the Space Unallocated

The space intended for Linux Mint must remain **Unallocated**.

* Do not create a new NTFS volume.
* Do not format the space.
* Do not assign a drive letter.
* Do not modify existing EFI or recovery partitions.

If a new NTFS volume was accidentally created in the intended space, right-click that specific volume and select **Delete Volume** to return it to unallocated space. Only do this after confirming that it is the newly created volume and contains no needed data.

## 4. Verify the Disk Layout

Before proceeding, check that:

* Windows 11 remains on the existing `C:` partition.
* The EFI System Partition and recovery partition remain intact.
* The intended Linux space is shown as **Unallocated**.
* The unallocated space is on the disk intended for Linux Mint.

The Linux installer will handle the Linux filesystem and partition configuration. Review the installer's proposed disk changes carefully before confirming them.

## Next Step

[Configure BIOS/UEFI](BIOS.md)
