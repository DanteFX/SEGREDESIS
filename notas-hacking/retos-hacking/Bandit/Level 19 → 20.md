
# Level 19→ Level 20

## Objetivo
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.
## Datos de acceso
bandit.labs.overthewire.org
bandit19
awhqfNnAbc1naukrpqDYcF95h7HoMTrC

## Solución
```bash
bandit19@bandit:~$ ls -la
bandit20-do
bandit19@bandit:~$ ^[[200~./bandit20-do id~
-bash: ./bandit20-do: No such file or directory
bandit19@bandit:~$ ./bandit20-do id
uid=11019(bandit19) gid=11019(bandit19) euid=11020(bandit20) groups=11019(bandit19)
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit19@bandit:~$ 

```


## Notas adicionales

## Referencias
[setuid on Wikipedia](https://en.wikipedia.org/wiki/Setuid)