
# Level 10→ Level 11

## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data.
## Datos de acceso
bandit.labs.overthewire.org
bandit10
truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

## Solución
cat data.txt | base64 -d
IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

## Notas adicionales

## Referencias
[Base64 on Wikipedia](https://en.wikipedia.org/wiki/Base64)