---
tags:
  - command/linux
  - pen-drive
links: 
reference: "[[dd]]"
path: Notes
created: 2023-09-16 19:29
modified: 2023-09-16 19:29
---
## lsblk 

Command used to display the partitions of your system.
```bash
λ lsblk                                                                     [~/Downloads] 
NAME         MAJ:MIN RM   SIZE RO TYPE  MOUNTPOINTS
sda            8:0    0   2,7T  0 disk  
└─sda1         8:1    0   2,7T  0 part  
nvme0n1      259:0    0 953,9G  0 disk  
├─nvme0n1p1  259:1    0   1,4G  0 part  /boot
└─nvme0n1p2  259:2    0 952,5G  0 part  
  └─cryptlvm 254:0    0 952,5G  0 crypt /
```

