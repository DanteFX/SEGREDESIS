## Descripción
Can you get the flag?Run this [Python program](https://artifacts.picoctf.net/c/430/bloat.flag.py) in the same directory as this [encrypted flag](https://artifacts.picoctf.net/c/430/flag.txt.enc)

## Solución
Hay que comentar sys.exit(0)
``` python
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $nano bloat.flag.py 
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $python3 bloat.flag.py 
Please enter correct password for flag: 
That password is incorrect
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $nano 
Display all 180 possibilities? (y or n)^C
┌─[✗]─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $nano bloat.flag.py 
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $python3 bloat.flag.py 
Please enter correct password for flag: happychance
Welcome back... your flag, user:
picoCTF{d30bfu5c4710n_f7w_5e14b257}
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $



```
picoCTF{d30bfu5c4710n_f7w_5e14b257}