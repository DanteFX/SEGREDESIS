## Descripción
Can you get the flag?Download this [binary](https://artifacts.picoctf.net/c/117/gdbme).Here's the test drive instructions:

-   `$ chmod +x gdbme`
-   `$ gdb gdbme`
-   `(gdb) layout asm`
-   `(gdb) break *(main+99)`
-   `(gdb) run`
-   `(gdb) jump *(main+104)`
## Solución


``` python
│   0x555555555305 <main+62>        movabs $0x6630624760433530,%rax            │
│   0x5555555550a0 <__cxa_finalize@plt>     endbr64                            │
│   0x5555555550a4 <__cxa_finalize@plt+4>   bnd jmp *0x2f4d(%rip)        # 0x5 │
│   0x5555555550ab <__cxa_finalize@plt+11>  nopl   0x0(%rax,%rax,1)            │
│   0x5555555550b0 <free@plt>               endbr64                            │
│   0x5555555550b4 <free@plt+4>             bnd jmp *0x2ee5(%rip)        # 0x5 │
│   0x5555555550bb <free@plt+11>            nopl   0x0(%rax,%rax,1)            │
│   0x5555555550c0 <putchar@plt>            endbr64                            │
│   0x5555555550c4 <putchar@plt+4>          bnd jmp *0x2edd(%rip)        # 0x5 │
│   0x5555555550cb <putchar@plt+11>         nopl   0x0(%rax,%rax,1)            │
│   0x5555555550d0 <strlen@plt>             endbr64                            │
│   0x5555555550d4 <strlen@plt+4>           bnd jmp *0x2ed5(%rip)        # 0x5 │
│   0x5555555550db <strlen@plt+11>          nopl   0x0(%rax,%rax,1)            │
│   0x5555555550e0 <__stack_chk_fail@plt>   endbr64                            │
native process 82149 In: main                          L??   PC: 0x55555555532a 
BreakpoNo process In:                                              L??   PC: ??
Breakpoint 1, 0x000055555555532a in main ()
(gdb) 
(gdb) jump *(main+104)Continuing at 0x55555555532f.
picoCTF{d3bugg3r_dr1v3_7776d758}
[Inferior 1 (process 82149) exited normally]
The program is not being run.
(gdb) Quit
(gdb) 

```
picoCTF{d3bugg3r_dr1v3_7776d758}