
# Level 12→ Level 13

## Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)
## Datos de acceso
bandit.labs.overthewire.org
bandit12
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

## Solución
```bash
ls
cat data.txt | xxd -r | file -
cat data.txt | xxd -r | zcat | file -
cat data.txt | xxd -r | zcat | bzcat | file -
cat data.txt | xxd -r | zcat | bzcat | zcat | file -
cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | file -
cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | file -
cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | file -
cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | file -
cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat | file -
8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
```
## Notas adicionales

## Referencias
[Hex dump on Wikipedia](https://en.wikipedia.org/wiki/Hex_dump)