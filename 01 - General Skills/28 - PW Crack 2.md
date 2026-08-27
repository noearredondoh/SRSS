## Descripción

Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.

## Solución

```
NoeAH-academy@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.py
--2026-08-27 01:50:53--  https://artifacts.picoctf.net/c/15/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.95, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py                                                  100%[========================================================================================================================================>]     914  --.-KB/s    in 0s      

2026-08-27 01:50:53 (361 MB/s) - 'level2.py' saved [914/914]

NoeAH-academy@webshell:~$ https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
-bash: https://artifacts.picoctf.net/c/15/level2.flag.txt.enc: No such file or directory
NoeAH-academy@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
--2026-08-27 01:51:28--  https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.95, 3.160.5.40, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc                                        100%[========================================================================================================================================>]      31  --.-KB/s    in 0s      

2026-08-27 01:51:28 (16.7 MB/s) - 'level2.flag.txt.enc' saved [31/31]

NoeAH-academy@webshell:~$ python3 level2.py
Please enter correct password for flag: hola
That password is incorrect
NoeAH-academy@webshell:~$ nano level2.py
NoeAH-academy@webshell:~$ python3 level2.py
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
```

## Notas adicionales

Se analizó el código en Python y se convirtieron los valores hexadecimales de la función `chr()` a sus caracteres correspondientes para obtener la contraseña y mostrar la bandera.

## Referencias