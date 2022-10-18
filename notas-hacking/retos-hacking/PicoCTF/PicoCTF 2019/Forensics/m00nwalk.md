## Descripción
Decode this [message](https://jupiter.challenges.picoctf.org/static/14393e18d98fedbaedbc28896d7ef31a/message.wav) from the moon.

## Solución

Se tiene que decodificar la imagen SSTV con una herramienta llamada "QSSTV".

``` bash
┌─[dantefx@dantefx-Inspiron5481]─[~]
└──╼ $paplay -d virtual-cable message.wav 
```

picoCTF{beep_boop_im_in_space}