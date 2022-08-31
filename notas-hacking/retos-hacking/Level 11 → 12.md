
# Level 11→ Level 12

## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.
## Datos de acceso
bandit.labs.overthewire.org
bandit11
IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

## Solución
ls
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
## Notas adicionales

## Referencias
[Rot13 on Wikipedia](https://en.wikipedia.org/wiki/Rot13)