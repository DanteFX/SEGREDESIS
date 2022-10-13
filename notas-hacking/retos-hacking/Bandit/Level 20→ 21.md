
# Level 20→ Level 21

## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).
## Datos de acceso
bandit.labs.overthewire.org
bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT

## Solución
```bash
bandit20@bandit:~$ nc -lvp 3000 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 309526
bandit20@bandit:~$ Listening on 0.0.0.0 3000
bandit20@bandit:~$ ./suconnect 3000
Connection received on localhost 49622
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
[1]+  Done                    nc -lvp 3000 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit20@bandit:~$ 
```


## Notas adicionales

## Referencias
