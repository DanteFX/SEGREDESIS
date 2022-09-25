### PW Crack 3

## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/23/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/23/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/23/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución
```bash
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $nano level3.py
'
import hashlib

### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c>
###############################################################################

flag_enc = open('level3.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level3.hash.bin', 'rb').read()


def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
  pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()


def level_3_pw_check(user_pw):
    #user_pw = input("Please enter correct password for flag: ")
    user_pw_hash = hash_pw(user_pw)
    
    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]

for pss in pos_pw_list:
        level_3_pw_check(pss)
'
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $python3 level3.py level3.flag.txt.enc 
That password is incorrect
That password is incorrect
That password is incorrect
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}
That password is incorrect
That password is incorrect
That password is incorrect

```


## Notas adicionales
El código que válida las contraseñas tenia algunas contraseñas almacenadas, entonces se modificó el código eliminando la entrada de usuario y con un for obteniendo las contraseñas almacenadas y llamando a la función level_3_pw_check(pss) con cada contraseña hasta que alguna sea la correcta.

## Referencias
