## Descripción
The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/27dd5548b14661f65ce3ac6a8a8f575b/need-for-speed).
## Solución

``` python
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $chmod +x need-for-speed && ./need-for-speed
Keep this thing over 50 mph!
============================

Creating key...
Not fast enough. BOOM!
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $gdb ./need-for-speed
GNU gdb (Debian 10.1-1.7) 10.1.90.20210103-git
Copyright (C) 2021 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from ./need-for-speed...
(No debugging symbols found in ./need-for-speed)
(gdb) handle SIGALRM ignore
Signal        Stop	Print	Pass to program	Description
SIGALRM       No	No	No		Alarm clock
(gdb) r
Starting program: /home/dantefx/Descargas/need-for-speed 
Keep this thing over 50 mph!
============================

Creating key...
Finished
Printing flag:
PICOCTF{Good job keeping bus #1f2ac4ec speeding along!}
[Inferior 1 (process 60911) exited normally]
(gdb) 

```

PICOCTF{Good job keeping bus #1f2ac4ec speeding along!}