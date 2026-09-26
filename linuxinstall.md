# Install Linux Mint

This guide covers installing Linux Mint alongside an existing Windows 11 installation using the previously prepared unallocated disk space.

## 1. Boot from the Linux Mint USB

1. Insert the Linux Mint USB.
2. Restart the computer.
3. Open the boot menu by pressing F12.
4. Select the **UEFI** entry for the Linux Mint USB.
5. Select **Start Linux Mint**.

Linux Mint will start in a live environment without immediately changing the Windows installation.

## 2. Start the Installer

Once the Linux Mint desktop loads:

1. Open **Install Linux Mint**.
2. Select the required language.
3. Select the keyboard layout.
4. Configure the network connection if required.
5. Continue through the installer until the installation type is displayed.

## 3. Select the Installation Type

The available installation options depend on the existing disk layout and Linux Mint release.

When an option to install Linux Mint alongside Windows is available, review the proposed partition changes carefully.

Alternatively, use **manual partitioning** when specific control over the Linux partitions is required.

> **Important:** Do not continue until the installation summary has been checked. The Windows `C:` partition, EFI System Partition, and recovery partition should not be accidentally selected for deletion or formatting.

## 4. Select the Linux Space

The space prepared in `Volume.md` should appear as unallocated space.

For a manual installation, the Linux space can be assigned to the Linux filesystem.

A typical basic installation can use:

```text
Filesystem: ext4
Mount point: /
```

A separate swap partition is not normally required for a basic installation because Linux Mint can use a swap file.

## 5. EFI System Partition

The existing EFI System Partition should be reused by the Linux installation rather than creating an unnecessary additional EFI partition.

The EFI partition is normally:

```text
FAT32
Approximately 500 MB
EFI System Partition
```

Do **not** format the existing Windows EFI System Partition.

## 6. Confirm the Changes

Before starting the installation, carefully review the final disk summary.

Confirm that:

* Windows 11 remains intact.
* The Windows `C:` partition is not being formatted.
* The EFI System Partition is not being formatted.
* The Windows recovery partition is not being deleted.
* The intended Linux space is being used for Linux.
* The proposed changes match the intended dual-boot layout.

Only proceed once the disk changes have been verified.

## 7. Complete the Installation

Continue through the installer:

1. Select the time zone.
2. Create the Linux user account.
3. Set the computer name and password.
4. Review the installation summary.
5. Start the installation.
6. Wait for the installation to complete.
7. Restart the computer when prompted.
8. Remove the USB when instructed.

## 8. Boot into the Dual-Boot Menu

After restarting, the system should boot through the configured UEFI bootloader.

A GRUB menu may provide entries for:

```text
Linux Mint
Windows Boot Manager
```

Select **Linux Mint** to start Linux Mint or **Windows Boot Manager** to start Windows 11.

The exact menu entries and appearance can vary depending on the Linux Mint release and the system's existing UEFI configuration.

## 9. Verify Both Operating Systems

After the installation:

### Linux Mint

Boot into Linux Mint and verify that:

* The desktop loads normally.
* The installed storage is detected.
* Network connectivity works.
* The Linux filesystem is mounted correctly.

### Windows 11

Restart and select **Windows Boot Manager**.

Verify that:

* Windows starts normally.
* The `C:` drive is intact.
* Personal files are accessible.
* Windows Disk Management shows the Linux partition as an unrecognised Linux filesystem rather than an NTFS Windows volume.
