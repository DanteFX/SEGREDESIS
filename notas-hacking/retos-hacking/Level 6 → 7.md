
# Level 6→ Level 7

## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size

## Datos de acceso
bandit.labs.overthewire.org
bandit6
DXjZPULLxYr17uwoI01bNLQbtFemEgo7

## Solución
![[Pasted image 20220828095020.png]]
## Notas adicionales
Para encontrar un archivo de cierto usuario, cierto grupo y cierto tamaño se necesita find con parametros: -user -group -size
Por ejemplo: find / -readable -user bandit7 -group bandit6 -size 33c


## Referencias