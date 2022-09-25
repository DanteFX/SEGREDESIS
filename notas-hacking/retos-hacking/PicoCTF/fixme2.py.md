### fixme2.py

## Objetivo
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/65/fixme2.py)
## Solución
```bash
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $python3 fixme2.py 
  File "/home/dantefx/Descargas/fixme2.py", line 22
    if flag = "":
            ^
SyntaxError: invalid syntax
┌─[✗]─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $nano fixme2.py 
'
import random

def str_xor(secret, key):
    #extend key to secret length
    new_key = key

    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c>


flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21>

  
flag = str_xor(flag_enc, 'enkidu')

# Check that flag is not empty
if flag == "":
  print('String XOR encountered a problem, quitting.')
else:
  print('That is correct! Here\'s your flag: ' + flag)
'

┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $python3 fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}

```

## Notas adicionales

## Referencias
