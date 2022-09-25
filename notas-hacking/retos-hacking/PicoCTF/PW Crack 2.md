### PW Crack 2

## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level2.flag.txt.enc) in the same directory too.
## Solución
```bash
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $nano level2.py 
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $python3
Python 3.9.2 (default, Feb 28 2021, 17:03:44) 
[GCC 10.2.1 20210110] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65))
39ce
>>> exit()
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $python3 level2.py level2.flag.txt.enc 
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}

```


## Notas adicionales
El checador de contraseña está códificado en hex sumando cada uno para obtener la contraseña, entonces decodificando a char cada uno sale la contraseña: "print(chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65))"
## Referencias
