## Descripción
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values)

## Solución
``` bash
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $cat values
Decrypt my super sick RSA:
c: 964354128913912393938480857590969826308054462950561875638492039363373779803642185
n: 1584586296183412107468474423529992275940096154074798537916936609523894209759157543
e: 65537┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $python3
```
``` python
Python 3.9.2 (default, Feb 28 2021, 17:03:44) 
[GCC 10.2.1 20210110] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> c = 964354128913912393938480857590969826308054462950561875638492039363373779803642185
>>> p =  2434792384523484381583634042478415057961
>>> q =  650809615742055581459820253356987396346063
>>> n = p * q
>>> n
1584586296183412107468474423529992275940096154074798537916936609523894209759157543
>>> e = 65537
>>> tn = (p-1)*(q-1)
>>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse
>>> d = inverse(e,tn)
>>> m = pow(c,d,n)
>>> m
13016382529449106065927291425342535437996222135352905256639684640304028661985917
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_73918962}'
>>
```

picoCTF{sma11_N_n0_g0od_73918962}