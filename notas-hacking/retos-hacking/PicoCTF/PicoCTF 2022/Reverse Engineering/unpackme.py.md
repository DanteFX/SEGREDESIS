## Descripción
Can you get the flag?Reverse engineer this [Python program](https://artifacts.picoctf.net/c/466/unpackme.flag.py).
## Solución

Hay que imprimir plain.decode()
``` python
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $python3 unpackme.flag.py 

pw = input('What\'s the password? ')

if pw == 'batteryhorse':
  print('picoCTF{175_chr157m45_85f5d0ac}')
else:
  print('That password is incorrect.')


```
picoCTF{175_chr157m45_85f5d0ac}