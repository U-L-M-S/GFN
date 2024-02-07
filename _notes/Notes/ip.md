---
tags:
  - command/linux
  - netzwerk/ip
  - netzwerk/gateway
  - netzwerk/subnet-mask
links: 
reference: "[[ipv4]]"
path: Notes
created: 2023-09-13 13:15
modified: 2023-09-13 13:15
---
## ip 
I's the command used to get the network card information. Most of the times used to get the [[IP Address]]. 

### Arguments
#### a
```bash
❯ ip a
```
output:
```bash
❯ ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host noprefixroute 
       valid_lft forever preferred_lft forever
2: wlan0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default qlen 1000
    link/ether ac:d5:64:8c:b9:d9 brd ff:ff:ff:ff:ff:ff
    inet 172.16.3.180/16 brd 172.16.255.255 scope global dynamic noprefixroute wlan0
       valid_lft 33488sec preferred_lft 33488sec
    inet 172.16.3.222/16 metric 600 brd 172.16.255.255 scope global secondary dynamic wlan0
       valid_lft 36715sec preferred_lft 36715sec
    inet6 fdab:9838:4b8:0:aed5:64ff:fe8c:b9d9/64 scope global mngtmpaddr noprefixroute 
       valid_lft forever preferred_lft forever
    inet6 2a02:8071:b586:e680:aed5:64ff:fe8c:b9d9/64 scope global dynamic mngtmpaddr noprefixroute 
       valid_lft 86385sec preferred_lft 43185sec
    inet6 fd11:e026:78d9:0:aed5:64ff:fe8c:b9d9/64 scope global dynamic mngtmpaddr noprefixroute 
       valid_lft 86385sec preferred_lft 43185sec
    inet6 fdab:9838:4b8::389/128 scope global dynamic noprefixroute 
       valid_lft 36846sec preferred_lft 36846sec
    inet6 2a02:8071:b586:e680:26c7:2c5d:57c4:7db4/64 scope global dynamic noprefixroute 
       valid_lft 86386sec preferred_lft 43186sec
    inet6 fd11:e026:78d9:0:59e9:cd5c:b429:765a/64 scope global dynamic noprefixroute 
       valid_lft 86386sec preferred_lft 43186sec
    inet6 fdab:9838:4b8:0:cb81:c3fd:c311:21b0/64 scope global noprefixroute 
       valid_lft forever preferred_lft forever
    inet6 2a02:8071:b587:89a0:f6ba:eaf1:6e2d:d452/64 scope global dynamic noprefixroute 
       valid_lft 6870sec preferred_lft 3270sec
    inet6 2a02:8071:b587:89a0:aed5:64ff:fe8c:b9d9/64 scope global dynamic mngtmpaddr noprefixroute 
       valid_lft 6869sec preferred_lft 3269sec
    inet6 fe80::6a20:d37a:3506:53ab/64 scope link noprefixroute 
       valid_lft forever preferred_lft forever
```

#### route 
```bash
❯ ip route show | grep default
```
output :
```bash
❯ ip route show | grep default
default via 172.16.0.1 dev wlan0 proto dhcp src 172.16.3.180 metric 600 
default via 172.16.0.1 dev wlan0 proto dhcp src 172.16.3.222 metric 600 
```
In this case I have two gateways, but the second is a backup (just ignore it) and the [[IP Address]] of my gateway is `172.16.0.1`. 