---
tags:
  - netzwerk/host
links: 
reference: "[[Netzwerk]]"
path: Notes
created: 2023-09-14 16:34
modified: 2023-09-14 16:34
---
## Hosts Herausfinden 
Nehmen wir an du hast diese Informationen:
- [[IP Address]]:192.168.32.5/24
- [[Subnet Mask]]:255.255.255.0

um die Anzahl von mögliche **Hosts**([[Network Portion und Host#^099b19]]) zu berechnen muss du nur den [[Subnet Mask]] in [[Binärzahlen]] darstellen und dann die Formel verwenden: $2^{{n}}-2$ wobei **n** die Anzahl von Nullen ist.

255.255.255.0 -> 11111111.11111111.11111111.00000000 -> (8 Nullen)

$$2^{{8}}-2=254$$ 
>[!info] Reminder
> Wir müssen 2 subtrahieren da wir 2 [[IP Address]] für Network Address und Broadcast Address brauchen.


