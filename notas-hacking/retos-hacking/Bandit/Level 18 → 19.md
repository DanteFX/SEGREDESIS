
# Level 18→ Level 19

## Objetivo
The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.
## Datos de acceso
bandit.labs.overthewire.org
bandit18
hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg

## Solución
```bash
┌─[dantefx@dantefx-Inspiron5481]─[~]
└──╼ $ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password: 
awhqfNnAbc1naukrpqDYcF95h7HoMTrC


```


## Notas adicionales

## Referencias