# Based

## Objetivo
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 15130`.

## Solución
Ventana 1
```bash
┌─[dantefx@dantefx-Inspiron5481]─[~]
└──╼ $nc jupiter.challenges.picoctf.org 15130
Let us see how data is stored
falcon
Please give the 01100110 01100001 01101100 01100011 01101111 01101110 as a word.
...
you have 45 seconds.....

Input:
falcon
Please give me the  154 151 147 150 164 as a word.
Input:
light
Please give me the 6368616972 as a word.
Input:
chair
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_02167de8}

```
Ventana 2
```bash
┌─[dantefx@dantefx-Inspiron5481]─[~]
└──╼ $nano based.py 
while True:
    n = input()
    s = n.split(' ')
    if len(s) == 1:
        s = []
        for c in range(0, len(n), 2):
            s.append(n[c:c+2])
    for b in [2, 8, 16, 64]:
        for i in range(len(s)):
            try:
                print(chr(int(s[i], b)), end='')
            except:
                print('.', end='')
        print()
┌─[dantefx@dantefx-Inspiron5481]─[~]
└──╼ $python3 based.py 
01100110 01100001 01101100 01100011 01101111 01101110
falcon
񈁈񈀁񈉀񈀉񈉉񈉈
......
......
154 151 147 150 164
.....
light
ŔőŇŐŤ
.....
6368616972
.....
3.1.:
chair
.....

```

## Notas adicionales

## Referencias
