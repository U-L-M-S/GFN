---
tags:
  - collax
  - 2023y
links: 
reference: 
path: Notes
created: 2023-10-03 17:58
modified: 2023-10-03 17:58
---
## # Stonith

>Shoot The Other Node In The Head

Wird die Arbeit eines [Knotens](https://de.wikipedia.org/wiki/Netzwerkelement "Netzwerkelement") (einzelner Computer) in einem [Computercluster](https://de.wikipedia.org/wiki/Computercluster) wegen eines Fehlers von einem anderen Knoten übernommen, muss der fehlerhafte Knoten an der Weiterarbeit gehindert werden. Die einfache Idee hinter STONITH ist, den fehlerhaften Knoten durch automatisches Unterbrechen der Stromzufuhr oder dem absichtlichen Auslösen einer [Kernel panic](https://de.wikipedia.org/wiki/Kernel_panic "Kernel panic")[[1]](https://de.wikipedia.org/wiki/STONITH#cite_note-1) an der Weiterarbeit zu hindern.

>[!note] 
>Mit andere Wörter, man hat zwei Servers, mit den selbe Inhalt, und sobald einer auf irgendwelche Grund nicht mehr funktioniert, wird  diese von den andere Server gekill und diese Server übernimmt seine Aufgabe. Somit erschafft man die Möglichkeit weiter zu arbeiten, ohne technische Problemen zu haben. 