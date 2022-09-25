### ### First Grep

## Objetivo
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file)? This would be really tedious to look through manually, something tells me there is a better way.


## Solución
```bash
┌─[✗]─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $strings file | grep pico
picoCTF{grep_is_good_to_find_things_f77e0797}

```


## Notas adicionales

## Referencias
grep [tutorial](https://ryanstutorials.net/linuxtutorial/grep.php)