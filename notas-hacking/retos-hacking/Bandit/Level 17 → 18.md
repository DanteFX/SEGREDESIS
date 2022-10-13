
# Level 17→ Level 18

## Objetivo
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**
## Datos de acceso
bandit.labs.overthewire.org
bandit17
bandit17.key

## Solución
```bash
bandit17@bandit:~$ diff passwords.new passwords.old
42c42
< hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
---
> 09wUIyMU4YhOzl1Lzxoz0voIBzZ2TUAf
bandit17@bandit:~$ 

```


## Notas adicionales

## Referencias