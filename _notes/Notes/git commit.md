Tags: #git/commit
Links: 
Reference:
Path: Notes
Created: 2023-08-04 15:36
modified: 2023-08-04 15:36
___
## Git commit

^657b9a

```bash
git commit -m "this is a commit"
```

Mit dem Befehl `git commit` und der Nachricht `this is a commit` kannst du einen Save Point speichern. Das bedeutet, hier wird ein Save Point gesetzt, und mit dem Befehl [[git log]] können sogar alle deine Save Points eingesehen werden. Du kannst dann mit dem Befehl [[git checkout]] in der Zeit zurückkehren.

>[!tip] 
>Du kannst ```git commit -m "Titel #ENTER Kurz Beschreibung #ENTER"```
>eingeben. Somit  wird in deinen GitHub so aussehen:
>![[../../Resources/Files/IMGs/Pasted image 20230804162548.png]]
>![[../../Resources/Files/IMGs/Pasted image 20230804162651.png]]

```bash
git commit --amend
```

Auf diese Weise kannst du Informationen zu einem Commit hinzufügen, anstatt einen neuen Commit zu erstellen.