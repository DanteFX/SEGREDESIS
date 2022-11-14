## Descripción
Download this image file and find the flag.

-   [Download image file](https://artifacts.picoctf.net/c/138/drawing.flag.svg)

## Solución
``` bash
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $strings drawing.flag.svg| grep tspan
       id="text3723"><tspan
         id="tspan3748">p </tspan><tspan
         id="tspan3754">i </tspan><tspan
         id="tspan3756">c </tspan><tspan
         id="tspan3758">o </tspan><tspan
         id="tspan3760">C </tspan><tspan
         id="tspan3762">T </tspan><tspan
         id="tspan3764">F { 3 n h 4 n </tspan><tspan
         id="tspan3752">c 3 d _ d 0 a 7 5 7 b f }</tspan></text>
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $picoCTF{3nh4nc3d_d0a757bf}


```
picoCTF{3nh4nc3d_d0a757bf}