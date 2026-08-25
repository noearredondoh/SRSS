## Descripcion

Additional details appear once you launch your instance.

The work computer is running SSH. We've been given a script which performs some basic calculations, explore the script and find a flag.

Hostname: saturn.picoctf.net Port: 55167 Username: picoplayer Password: password
## Solucion
```
ssh picoplayer@saturn.picoctf.net -p 55167
```

```
NoeAH-academy@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 56167
ssh: connect to host saturn.picoctf.net port 56167: Connection refused
NoeAH-academy@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 55167
The authenticity of host '[saturn.picoctf.net]:55167 ([13.59.203.175]:55167)' can't be established.
ED25519 key fingerprint is SHA256:DiJcS90U9QussLS8HLR6l6BGJb5eCA0vRmA18IvDvw8.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:55167' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 
Permission denied, please try again.
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.6 LTS (GNU/Linux 6.17.0-1019-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

picoplayer@challenge:~$ man useless

useless
     useless, -- This is a simple calculator script

SYNOPSIS
     useless, [add sub mul div] number1 number2

DESCRIPTION
     Use the useless, macro to make simple calulations like addition,subtraction, multiplication and division.

Examples
     ./useless add 1 2
       This will add 1 and 2 and return 3

     ./useless mul 2 3
       This will return 6 as a product of 2 and 3

     ./useless div 6 3
       This will return 2 as a quotient of 6 and 3

     ./useless sub 6 5
       This will return 1 as a remainder of substraction of 5 from 6

Authors
     This script was designed and developed by Cylab Africa

     picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_3823}
```

```
picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_3823}
```

## Notas adicionales
man - te proporciona un munual de ayuda completo de un camando o ejecutable si es que hay

## Referencias
https://webshell.cylabacademy.org/