---
tags:
  - netzwerk/ip/ipv4
links: 
reference: "[[IP Address]]"
path: Notes
created: 2023-09-13 10:14
modified: 2023-09-13 10:14
---
## IPv4 
32-bit-Binärzahlen, die in Dezimal dargestellt werden und mit "**.**"  getrennt sind.  

	**192.168.42.98**

| 192 | 168 | 42 | 98 |
| :---: | :---: | :---: | :---: |
| 11000000 | 10101000 | 00101010 | 01100010 |

mit andere Wörtern wir können 2³²(4,3 Milliarden) [[IP Address]] haben, da  es von 0.0.0.0 bis 255.255.255.255 sein kann.
Obwohl man eine [[static]] IP Address haben kann, die meisten von denen werden durch den Router vergeben (automatisch).

>[!important] 
>Bei **ALLEN** [[Netzwerk]] müssen **IMMER** zwei IPs reserviert sein.
>
>1- Network Address 
>
>2- Brodcast Address

Mit andere Wörter wenn ich ein [[IP Address]] wie 192.168.1.204 und ein [[gateway]] wie 255.255.255.0 habe. Dann kann ich insgesamt 256 [[IP Address]] haben [192.168.1.**0**, 192.168.1.**1**, 192.168.1.**2**, ..., 192.168.1.**255** ]. 

Nützen darf ich nur 253. Das sind alle die zwischen **1** und  **254** sind. 
Da 192.168.1.0 reserviert ist, für den Netzwerk Address und soeben 192.168.1.255 für den Broadcast Address.
### IP finden
#### Linux
![[ip#ip a]]

Hier wird angezeigt, dass man zwei Netzkarten hat (1 und 2). Wobei `lo` steht für die Netzwerk via Kabel und `wlan0` via [[Wi-Fi]]. 
Mein [[IP Address]] lautet: `127.16.3.180`.

#### Windows
![[ipconfig#ipconfig]]
Hier kannst du sehen, dass mein IP (`Wlan`) `192.168.0.200` ist
### Klassen
IPv4 wurde in 5 Klassen unterteilt:

|          | -   | Range |  Subnet Mask   | 
| :-------:| --- | :---: | :---: |
| Klasse A | -   | 1.0.0.0 - 126.255.255.255 | *255*.0.0.0     |
| Klasse B | -   | 128.0.0.0 - 191.255.0.0 | *255.255*.0.0     |
| Klasse C | -   | 192.0.0.0 - 223.255.255.0 | *255.255.255*.0     |
| Klasse D | -   | 224.0.0.0 - 239.255.255.255 |     |
| Klasse E | -   | 240.0.0.0 - 255.255.255.255      |     |

^872578

>[!important] 
>
Heutzutage wird meistens **Klasse C** bei die meisten Router verwendet, die man zuhause hat.


>[!tip] There is not place like home
>Zwischen Klasse A und B sind die Adressen 127.0.0.0 nicht gelistet. Sie sind die [[loop back address]]