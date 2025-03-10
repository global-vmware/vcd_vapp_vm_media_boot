# Terraform Module Comparison: `vcd_vapp_vm` vs `vcd_vapp_vm_media_boot`

## **Table of Contents**
- [Introduction](#introduction)
- [1. New Variables in `vcd_vapp_vm_media_boot`](#1-new-variables-in-vcd_vapp_vm_media_boot)
- [2. New Resources and Enhancements](#2-new-resources-and-enhancements)
- [3. Modifications in Existing Resources](#3-modifications-in-existing-resources)
- [4. Summary of Key Enhancements](#4-summary-of-key-enhancements)

---

## **Introduction**
This document highlights the differences between the [vcd_vapp_vm](https://github.com/global-vmware/vcd_vapp_vm) and [vcd_vapp_vm_media_boot](https://github.com/global-vmware/vcd_vapp_vm_media_boot) Terraform modules. The primary focus is on new variables, resources, and code enhancements introduced in the `vcd_vapp_vm_media_boot` module.

---

## **1. New Variables in `vcd_vapp_vm_media_boot`**
The following variables were added in the `vcd_vapp_vm_media_boot` module along with their default values:

- `boot_catalog_org_name` (default: `""`)
- `boot_catalog_name` (default: `""`)
- `inserted_media_iso_name` (default: `""`)
- `inserted_media_eject_force` (default: `true`)
- `boot_iso_image_name` (default: `""`)
- `vm_os_type` (default: `""`)
- `vm_hw_version` (default: `""`)
- `vm_firmware` (default: `"bios"`)
- `vm_boot_delay` (default: `0`)
- `vm_boot_retry_enabled` (default: `false`)
- `vm_boot_retry_delay` (default: `0`)
- `vm_efi_secure_boot` (default: `false`)
- `vm_enter_bios_setup_on_next_boot` (default: `false`)
- `internal_disks` (default: `[]`)
- `vm_internal_disk_allow_vm_reboot` (default: `true`)

---

## **2. New Resources and Enhancements**
### **New Resources:**
- `vcd_inserted_media` (`media_iso`)
- `vcd_vm_internal_disk` (`internal_disk`)

### **Enhanced Configurations:**
- **Boot Options:** Added support for boot delays, retries, and secure boot.
- **`boot_image_id` Support:** Enables booting from a specified ISO.

---

## **3. Modifications in Existing Resources**
### **`vcd_vapp_vm` Enhancements:**
- New attributes for `os_type`, `hardware_version`, and `firmware`.
- Enhanced boot customization options.

### **Catalog and Media Enhancements:**
- Added support for boot catalog and ISO handling.

---

## **4. Summary of Key Enhancements**
1. **Boot from ISO Support**
2. **Enhanced Boot Options**
3. **Internal Disk Management**
4. **Granular Control over VM Configuration**

---
