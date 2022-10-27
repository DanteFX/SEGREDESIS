## Descripción
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/49743139fb7c10765dbf462d40987d2a/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/49743139fb7c10765dbf462d40987d2a/scrambled2.png)

## Solución
``` python
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/bin]
└──╼ $python3
Python 3.9.2 (default, Feb 28 2021, 17:03:44) 
[GCC 10.2.1 20210110] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from PIL import Image
>>> import numpy as np
>>> 
>>> image1 = np.asarray(Image.open("scrambled1.png"))
>>> image2 = np.asarray(Image.open("scrambled2.png"))
>>> 
>>> data = image1.copy() + image2.copy()
>>> 
>>> nueva = Image.fromarray(data)
>>> 
>>> nueva.save("out.png","PNG")
>>> 

```
Tambien se puede utilizar stegsolve para combinar las 2 imagenes, en este caso se resolvió con ADD

picoCTF{2a4d45c7}