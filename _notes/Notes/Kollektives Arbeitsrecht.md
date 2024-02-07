---
tags:
  - klausurrelevant
  - LF01V2
links: 
reference: 
path: Notes
created: 2024-02-07 06:19
modified: 2024-02-07 06:19
---
>Tarifvertrag, Betriebsvereinbarung.

Diese Art von Vertrag passiert immer nach Arbeitsvertrag und es sind Vereinbarungen zwischen der Arbeitgeber und eine Gruppe oder mehrere Gruppe von Angestellter.

>[!note] 
> Die Maschine-Mitarbeiter erhalten eine Lohnerhöhung von 10 Cent.

Diese Art von Vertrag kann auch passiert wenn eine Gruppe sich bessere Arbeitsbedingung vorderen. Somit können Streiks entstehen.

```mermaid
graph TB
A[Kündigung/Ablauf Der Tarifvertrag]
B[Aufstellung der neuenen Forderungen]
C[Einiegung auf neue TV <br> mit fest geleger Laufzeit]
D[Schlichtungsverfahren]
E[Urabstimmung]
F[Streik]
G[Ausperrung der Betrieb]
H[Neue Verhandlung]

A-->B
B-->if1{Einigung?}--ja-->C
if1{Einigung?}--nein-->D
D-->if2{Einigung?}--ja-->C
if2{Einigung?}--nein-->E
E-->if3{>75%?}--nein-->C
if3{>75%?}--ja-->F
F-->G
G-->H
H-->if4{>=25%?}--ja-->C
if4{>25%?}--nein-->F
```