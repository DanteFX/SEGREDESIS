### Static ain't always noise

## Objetivo
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static)? This [BASH script](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh) might help!
## Solución
```bash
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $cat static.ltdis.x86_64.txt | grep pico
┌─[✗]─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $cat static.ltdis.strings.txt | grep pico
   1020 picoCTF{d15a5m_t34s3r_f5aeda17}

```


## Notas adicionales

## Referencias
