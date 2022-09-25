#  plumbing

## Objetivo
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 14291`.
## Solución
```bash
┌─[dantefx@dantefx-Inspiron5481]─[~]
└──╼ $nc jupiter.challenges.picoctf.org 14291 | grep pico
picoCTF{digital_plumb3r_ea8bfec7}

```


## Notas adicionales
## Referencias
What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)