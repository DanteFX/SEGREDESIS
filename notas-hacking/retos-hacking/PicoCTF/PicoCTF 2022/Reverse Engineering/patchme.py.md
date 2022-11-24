## Descripción
Run this [Python program](https://artifacts.picoctf.net/c/388/patchme.flag.py) in the same directory as this [encrypted flag](https://artifacts.picoctf.net/c/388/flag.txt.enc).
## Solución
Hay que eliminar la condición de la contraseña para hacer un pass
``` python

┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $python3 patchme.flag.py 
Please enter correct password for flag: wff
Welcome back... your flag, user:
picoCTF{p47ch1ng_l1f3_h4ck_21d62e33}
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $

```
picoCTF{p47ch1ng_l1f3_h4ck_21d62e33}