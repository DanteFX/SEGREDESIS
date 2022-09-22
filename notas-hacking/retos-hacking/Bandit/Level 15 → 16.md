
# Level 15→ Level 16

## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.
Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…
## Datos de acceso
bandit.labs.overthewire.org
bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

## Solución
```bash
openssl s_client -connect localhost:30001
cluFn7wTiGryunymYOu4RcffSxQluehd
```
## Notas adicionales

## Referencias
-   [Secure Socket Layer/Transport Layer Security on Wikipedia](https://en.wikipedia.org/wiki/Secure_Socket_Layer)
-   [OpenSSL Cookbook - Testing with OpenSSL](https://www.feistyduck.com/library/openssl-cookbook/online/ch-testing-with-openssl.html)