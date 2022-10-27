## Descripción
We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/394/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

## Solución
``` bash

```
``` python
datos = open('message.txt').read().strip().split(' ')
datos = [int(i)%37 for i in datos]
flag = ''
for n in datos:
	if n in range(26):
		flag += chr(n+65)
	elif n in range(26,36):
		flag += chr(n+22)
	else:
		flag += "_"
print(flag)
```

