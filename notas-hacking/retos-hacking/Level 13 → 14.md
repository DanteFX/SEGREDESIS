
# Level 13→ Level 14

## Objetivo
The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on.
## Datos de acceso
bandit.labs.overthewire.org
bandit13
8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

## Solución
ls
ssh -i sshkey.private bandit14@localhost
cat /etc/bandit_pass/bandit14
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
## Notas adicionales

## Referencias
[SSH/OpenSSH/Keys](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)