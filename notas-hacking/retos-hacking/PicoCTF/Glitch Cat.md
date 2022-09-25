### Glitch Cat

## Objetivo
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 51109`
## Solución
```bash
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $nc saturn.picoctf.net 51109
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $python3
Python 3.9.2 (default, Feb 28 2021, 17:03:44) 
[GCC 10.2.1 20210110] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print('picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}')
picoCTF{gl17ch_m3_n07_bda68f75}
>>> 

```


## Notas adicionales

## Referencias
