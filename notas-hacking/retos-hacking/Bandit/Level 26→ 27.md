# Level 26→ Level 27

## Objetivo
   Logging in to bandit26 from bandit25 should be fairly easy The shell for user ban-  
   dit26 is not /bin/bash, but something else. Find out what it is, how it works and  
   how to break out of it.
## Datos de acceso
bandit.labs.overthewire.org
bandit26
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1

## Solución
``` bash
:set shell=/bin/bash
:shell
bandit26@bandit:~$ ls
bandit27-do  text.txt
bandit26@bandit:~$ ./bandit27-do id
uid=11026(bandit26) gid=11026(bandit26) euid=11027(bandit27) groups=11026(bandit26)
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit26@bandit:~$
```
## Notas adicionales

## Referencias
