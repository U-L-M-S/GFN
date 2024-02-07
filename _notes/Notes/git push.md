Tags: #git/push
Links: 
Reference:
Path: Notes
Created: 2023-08-06 16:18
modified: 2023-08-06 16:18
___
## git push
```bash
git push
```

Befehl wird verwendet um was bei mir (Lokal) steht an das Git verschickt wird.

>[!important] 
> In dein erste push, ist sehr normal, dass ein Fehler passiert.
> Wie Branch-Names [[git checkout#^5deb9e]] **ODER** dein Branch wurde noch nicht eingelegt `git push -u origin main`

>[!important] 
> Falls du ein Commit mit `git commit --amend` überschreibst. Wird dein Commit-Hash sich ändern (Lokal) und somit wird es nicht möglich sein zu pushen. 
> Was du machen kannst ist ein `git push --force origin <branch-name>` **ABER** es ist sehr gefährlich. Da du ein Commit löschen wird mit `--force`