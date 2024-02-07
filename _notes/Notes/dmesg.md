---
tags:
  - command/linux
  - hardware/information
links: 
reference: "[[dd]]"
path: Notes
created: 2023-09-16 19:06
modified: 2023-09-16 19:06
---
## dmesg

Linux command to show system informations. Most of the times used to display inputs.
This command is recommended to be use **BEFORE** [[dd]]

```bash
λ sudo dmesg                                                                 [~/Downloads] 
[sudo] Passwort für silcniu: 
[    0.000000] Linux version 6.5.3-arch1-1 (linux@archlinux) (gcc (GCC) 13.2.1 20230801, GNU ld (GNU Binutils) 2.41.0) #1 SMP PREEMPT_DYNAMIC Wed, 13 Sep 2023 08:37:40 +0000
[    0.000000] Command line: BOOT_IMAGE=/vmlinuz-linux root=UUID=31e0398d-1863-4043-84ee-9244cbd0a872 rw cryptdevice=UUID=8b0a4360-85b3-46e6-a2ab-737cf0e4a3ce:cryptlvm rootfstype=ext4 nvidia_drm.modeset=1 rd.driver.blacklist=nouveau modprob.blacklist=nouveau loglevel=3 quiet
[    0.000000] BIOS-provided physical RAM map:
[    0.000000] BIOS-e820: [mem 0x0000000000000000-0x000000000009ebff] usable
[    0.000000] BIOS-e820: [mem 0x000000000009ec00-0x000000000009ffff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000000e0000-0x00000000000fffff] reserved
[    0.000000] BIOS-e820: [mem 0x0000000000100000-0x0000000009d7ffff] usable
[    0.000000] BIOS-e820: [mem 0x0000000009d80000-0x0000000009ffffff] reserved
[    0.000000] BIOS-e820: [mem 0x000000000a000000-0x000000000a1fffff] usable
[    0.000000] BIOS-e820: [mem 0x000000000a200000-0x000000000a20afff] ACPI NVS
[    0.000000] BIOS-e820: [mem 0x000000000a20b000-0x000000000affffff] usable
[    0.000000] BIOS-e820: [mem 0x000000000b000000-0x000000000b01ffff] reserved
[    0.000000] BIOS-e820: [mem 0x000000000b020000-0x00000000db412fff] usable
[    0.000000] BIOS-e820: [mem 0x00000000db413000-0x00000000db558fff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000db559000-0x00000000db6d9fff] usable
[    0.000000] BIOS-e820: [mem 0x00000000db6da000-0x00000000dbaecfff] ACPI NVS
[    0.000000] BIOS-e820: [mem 0x00000000dbaed000-0x00000000dc890fff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000dc891000-0x00000000deffffff] usable
[    0.000000] BIOS-e820: [mem 0x00000000df000000-0x00000000dfffffff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000f8000000-0x00000000fbffffff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000fd000000-0x00000000ffffffff] reserved
[    0.000000] BIOS-e820: [mem 0x0000000100000000-0x000000041f37ffff] usable
```

### -w OR --follow

Same as before but it keeps listening.
```sudo dmesg -w
λ sudo dmesg -w                                                              [~/Downloads] 
[sudo] Passwort für silcniu: 
[    0.000000] Linux version 6.5.3-arch1-1 (linux@archlinux) (gcc (GCC) 13.2.1 20230801, GNU ld (GNU Binutils) 2.41.0) #1 SMP PREEMPT_DYNAMIC Wed, 13 Sep 2023 08:37:40 +0000
[    0.000000] Command line: BOOT_IMAGE=/vmlinuz-linux root=UUID=31e0398d-1863-4043-84ee-9244cbd0a872 rw cryptdevice=UUID=8b0a4360-85b3-46e6-a2ab-737cf0e4a3ce:cryptlvm rootfstype=ext4 nvidia_drm.modeset=1 rd.driver.blacklist=nouveau modprob.blacklist=nouveau loglevel=3 quiet
[    0.000000] BIOS-provided physical RAM map:
[    0.000000] BIOS-e820: [mem 0x0000000000000000-0x000000000009ebff] usable
[    0.000000] BIOS-e820: [mem 0x000000000009ec00-0x000000000009ffff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000000e0000-0x00000000000fffff] reserved
[    0.000000] BIOS-e820: [mem 0x0000000000100000-0x0000000009d7ffff] usable
[    0.000000] BIOS-e820: [mem 0x0000000009d80000-0x0000000009ffffff] reserved
```

