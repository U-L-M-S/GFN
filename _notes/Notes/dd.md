---
tags:
  - command/linux
  - "#dangerous"
links: 
reference: 
path: Notes
created: 2023-09-16 19:18
modified: 2023-09-16 19:18
---
## dd 

Command to create a bootable usb.  
Be careful otherwise you can rewrite you system partition.
```bash
sudo dd if=file.iso of=/dev/pendrive status=progress
```

Be careful!! `of=/dev/pendrive` is the name of your pen drive. If you select something else (Like the partition of your system) <mark style="background: #FF5582A6;">it will break your system. </mark> Use the command [[dmesg]] and [[lsblk]] to check the name of your pen drive.