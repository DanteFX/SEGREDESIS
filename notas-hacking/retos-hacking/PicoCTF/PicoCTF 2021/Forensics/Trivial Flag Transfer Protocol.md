## Descripción
Figure out how they moved the [flag](https://mercury.picoctf.net/static/e4836d9bcc740d457f4331d68129a0bc/tftp.pcapng).

## Solución
``` bash
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/tfpt]
└──╼ $sudo steghide extract -sf ./picture3.bmp -p "DUEDILIGENCE"
ya existe el archivo "flag.txt". �lo sobreescribo? (s/n) s
anot� los datos extra�dos e/"flag.txt".
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/tfpt]
└──╼ $
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/tfpt]
└──╼ $cat flag.txt 
picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/tfpt]
└──╼ $

```
picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}