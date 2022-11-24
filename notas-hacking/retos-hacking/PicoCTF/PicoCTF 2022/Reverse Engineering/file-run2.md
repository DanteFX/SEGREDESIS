## Descripción
Another program, but this time, it seems to want some input. What happens if you try to run it on the command line with input "Hello!"?Download the program [here](https://artifacts.picoctf.net/c/353/run).
## Solución

``` python
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $chmod +x run && ./run
Run this file with only one argument.
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $./run one
Won't you say 'Hello!' to me first?
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $./run Hello!
The flag is: picoCTF{F1r57_4rgum3n7_f65ed63e}
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $



```
picoCTF{F1r57_4rgum3n7_f65ed63e}