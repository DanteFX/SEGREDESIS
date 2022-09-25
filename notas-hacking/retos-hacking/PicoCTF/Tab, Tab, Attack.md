### Tab, Tab, Attack

## Objetivo
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip)
## Solución
```bash
─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  

┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $cd Addadshashanammu/
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu]
└──╼ $ls
Almurbalarammi
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu]
└──╼ $cd Almurbalarammi/
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu/Almurbalarammi]
└──╼ $ls
Ashalmimilkala
┌─[✗]─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu/Almurbalarammi]
└──╼ $cd Ashalmimilkala/
┌─[✗]─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu/Almurbalarammi/Ashalmimilkala]
└──╼ $ls
Assurnabitashpi
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu/Almurbalarammi/Ashalmimilkala]
└──╼ $cd Assurnabitashpi/
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi]
└──╼ $ls
Maelkashishi
┌─[✗]─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi]
└──╼ $cd Maelkashishi/
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi]
└──╼ $ls
Onnissiralis
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi]
└──╼ $cd Onnissiralis/
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis]
└──╼ $ls
Ularradallaku
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis]
└──╼ $cd Ularradallaku/
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└──╼ $ls
fang-of-haynekhtnamet
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└──╼ $file fang-of-haynekhtnamet 
fang-of-haynekhtnamet: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=b71f20bc162221a31840f68a978261097ecadac2, not stripped
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└──╼ $./fang-of-haynekhtnamet 

*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_6f332f10}

```


## Notas adicionales

## Referencias
