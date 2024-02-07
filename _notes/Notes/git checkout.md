Tags: #git/checkout
Links: 
Reference:
Path: Notes
Created: 2023-08-06 00:52
modified: 2023-08-06 00:52
___
## git checkout

```bash
git checkout
```

>[!attention] 
>Gefährlicher Befehl.

Es bietet viele Möglichkeiten, die du mit diesem Befehl ausführen kannst. Hier sind einige nützliche Optionen:

```bash
git checkout <commit-hash>
``` 

^ff4e5f

Mit dem Befehl kannst du zu einem bestimmten Commit wechseln. Ich möchte dir jedoch **dringend** empfehlen, dass du, wenn du zu einem Commit zurückkehrst, einen neuen Branch erstellst. (Bild)

``` bash
git checkout -b <new-branch-name>
``` 

Somit erstellst du eine neue Brach und kannst deine vorherige Commits nicht überschreiben.
![[../../Resources/Files/IMGs/Pasted image 20230806113223.png]]

```bash
git checkout <branch-name>
```

^5deb9e

wechseln zu eine andere Branch.

```bash
git checkout -- <file-name>
```

Setzt eine bestimmte Datei wie es war (als es commited wurde).

```bash
git checkout .
git checkout -- .
```
Sie sehen ähnlich aus, machen fast das gleiche. 
- I) Dieser Befehl <mark style="background: #FFF3A3A6;">verwirft alle Änderungen</mark> in den veränderten Dateien im <mark style="background: #FFF3A3A6;">aktuellen Verzeichnis</mark>. Dateien werden auf die <mark style="background: #FFF3A3A6;">letzten Commit-Zustand zurückzusetzen</mark>.

- II) Es macht das selbe wie `git checkout .`, betrifft jedoch <mark style="background: #FFF3A3A6;">sämtliche Unterverzeichnisse.</mark>