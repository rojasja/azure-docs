---
 title: include file
 description: include file
 services: storage
 author: roygara
 ms.service: storage
 ms.topic: include
 ms.date: 03/27/2023
 ms.author: rogarana
 ms.custom: include file
---
- Premium SSD v2 disks can't be used as an OS disk.
- Currently, Premium SSD v2 disks can only be attached to zonal VMs.
- Currently, encryption at host isn't supported for Premium SSD v2 disks. You can still attach Premium SSD v2 disks to VMs where you have enabled encryption at host for disk types.
- Azure Disk Encryption (guest VM encryption via Bitlocker/DM-Crypt) isn't supported for VMs with Premium SSD v2 disks. We recommend you to use encryption at rest with platform-managed or customer-managed keys, which is supported for Premium SSD v2. 
- Currently, Premium SSD v2 disks can't be attached to VMs in Availability Sets.
- Azure Backup and Azure Site Recovery aren't supported for VMs with Premium SSD v2 disks.
- The size of a Premium SSD v2 can't be expanded without either deallocating the VM or detaching the disk.
