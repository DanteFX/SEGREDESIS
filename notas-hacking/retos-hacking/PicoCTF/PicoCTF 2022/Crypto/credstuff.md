## Descripción
We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it?Download the leak [here](https://artifacts.picoctf.net/c/534/leak.tar).The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.

## Solución
Hay que descomprimir y buscar el usuario , en los passwords buscamos la misma linea del usuario, y tiene unas llaves, despues lo pasamos a un decodificador caesar.

``` python

```

picoCTF{C7r1F_54V35_71M3}