## Descripción
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/2978e1270538613cd8181c7b0dabe9bd/dolls.jpg)

## Solución
``` bash
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $binwalk -e dolls.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378942, uncompressed size: 383937, name: base_images/2_c.jpg
651600        0x9F150         End of Zip archive, footer length: 22

┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $cd _dolls.jpg.extracted/
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted]
└──╼ $la
total 376K
drwxr-xr-x 1 dantefx dantefx   40 nov 13 21:42 .
drwxr-xr-x 1 dantefx dantefx 4.5K nov 13 21:42 ..
-rw-r--r-- 1 dantefx dantefx 371K nov 13 21:42 4286C.zip
drwxr-xr-x 1 dantefx dantefx   14 nov 13 21:42 base_images
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted]
└──╼ $cd base_images/
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images]
└──╼ $ls
2_c.jpg
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images]
└──╼ $binwalk -e 2_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196042, uncompressed size: 201444, name: base_images/3_c.jpg
383804        0x5DB3C         End of Zip archive, footer length: 22
383915        0x5DBAB         End of Zip archive, footer length: 22

┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images]
└──╼ $ls
2_c.jpg  _2_c.jpg.extracted
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images]
└──╼ $cd _2_c.jpg.extracted/
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted]
└──╼ $ls
2DD3B.zip  base_images
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted]
└──╼ $cd base_images/
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└──╼ $ls
3_c.jpg
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└──╼ $binwalk 3_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77650, uncompressed size: 79806, name: base_images/4_c.jpg
201422        0x312CE         End of Zip archive, footer length: 22

┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└──╼ $ls
3_c.jpg
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└──╼ $ls
3_c.jpg
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└──╼ $binwalk -e 3_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77650, uncompressed size: 79806, name: base_images/4_c.jpg
201422        0x312CE         End of Zip archive, footer length: 22

┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└──╼ $ls
3_c.jpg  _3_c.jpg.extracted
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└──╼ $cd _3_c.jpg.extracted/
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted]
└──╼ $ls
1E2D6.zip  base_images
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted]
└──╼ $cd base_images/
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└──╼ $binwalk -e 4_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v2.0 to extract, compressed size: 62, uncompressed size: 81, name: flag.txt
79784         0x137A8         End of Zip archive, footer length: 22

┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└──╼ $cd _4_c.jpg.extracted/
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└──╼ $ls
136DA.zip  flag.txt
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└──╼ $cat flag.txt 
picoCTF{4cf7ac000c3fb0fa96fb92722ffb2a32}┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└──╼ $


```
picoCTF{4cf7ac000c3fb0fa96fb92722ffb2a32}