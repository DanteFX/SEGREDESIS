### fixme1.py

## Objetivo
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/39/fixme1.py)
## Solución
```bash
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $python3 fixme1.py 
  File "/home/dantefx/Descargas/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
┌─[✗]─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $nano fixme1.py 
'import random



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
print('That is correct! Here\'s your flag: ' + flag)
'
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $python3 fixme1.py 
That is correct! Heres your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $

```


## Notas adicionales
Solo se recorrió una indentación atrás en la linea 20 "print('That is correct! Here\'s your flag: ' + flag)"
## Referencias
