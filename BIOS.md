# BIOS.md

# Configure BIOS/UEFI

Before starting the Linux Mint installation, verify that the system is configured to boot using **UEFI**.

## 1. Enter BIOS/UEFI

1. Restart the computer.
2. Enter the BIOS/UEFI setup using the manufacturer's key.
3. Common keys include `F2`, `Delete`, `F10`, or `Esc`.

The exact key and menu names depend on the computer manufacturer.

## 2. Verify UEFI Boot Mode

Locate the boot configuration settings.

Confirm that the system is using:

* **UEFI** boot mode
* **GPT** partitioning
* The existing Windows EFI System Partition

Avoid enabling **Legacy/CSM** boot mode when installing Linux alongside an existing UEFI Windows installation.

## 3. Check Secure Boot

Linux Mint can normally be installed on systems using Secure Boot.

Keep **Secure Boot enabled** unless the installation encounters a specific compatibility or boot issue that requires changing it.

If Secure Boot is changed, record the original setting so it can be restored if necessary.

## 4. Check Storage Configuration

Some systems use Intel RST/RAID storage configuration rather than AHCI.

If Linux Mint reports that the Windows storage device cannot be accessed because of Intel RST, the storage configuration may need to be changed.

> **Warning:** Changing RST/RAID to AHCI can prevent Windows from booting if Windows has not been prepared for the change. The exact procedure is system-dependent, so check the computer manufacturer's documentation before changing the setting.

If the system is already configured for AHCI and Linux Mint can access the disk, no storage-mode change is required.

## 5. Configure the Boot Order

Insert the Linux Mint USB created in the previous step.

Open the **Boot** section and ensure that the USB device can be selected as a UEFI boot device.

The boot menu may show an entry similar to:

```text
UEFI: USB Drive
```

Select the UEFI USB entry rather than a legacy/CSM entry.

## 6. Save and Reboot

Save the BIOS/UEFI changes and restart the computer.

Use the boot menu if necessary to select the Linux Mint USB.

The system should now boot into the Linux Mint installer.

## Next Step

[Install Linux Mint](Linuxinstall.md)
