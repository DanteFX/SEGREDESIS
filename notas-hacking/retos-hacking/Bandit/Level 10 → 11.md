
# Level 10→ Level 11

## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data.
## Datos de acceso
bandit.labs.overthewire.org
bandit10
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

## Solución
```bash
cat data.txt | base64 -d
IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```
## Notas adicionales

## Referencias
[Base64 on Wikipedia](https://en.wikipedia.org/wiki/Base64)