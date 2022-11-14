## Descripción
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/d1375e383810d8d957c04eef9e345732/cat.jpg)

## Solución
``` bash
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $exiftool cat.jpg
ExifTool Version Number         : 12.16
File Name                       : cat.jpg
Directory                       : .
File Size                       : 858 KiB
File Modification Date/Time     : 2022:11:13 22:51:15-06:00
File Access Date/Time           : 2022:11:13 22:51:13-06:00
File Inode Change Date/Time     : 2022:11:13 22:51:15-06:00
File Permissions                : rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $exiftool cat.jpg | grep License
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $exiftool cat.jpg | grep License | sed -e 's/.*: //' | base64 -d
picoCTF{the_m3tadata_1s_modified}┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]

```
picoCTF{the_m3tadata_1s_modified}