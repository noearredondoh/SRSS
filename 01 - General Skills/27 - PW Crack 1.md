## Descripción

Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.

- To view the file in the webshell, do: `$ nano level1.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución

```
NoeAH-academy@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.py
--2026-08-27 01:37:21--  https://artifacts.picoctf.net/c/11/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.95, 3.160.5.40, 3.160.5.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py                                                  100%[========================================================================================================================================>]     876  --.-KB/s    in 0s      

2026-08-27 01:37:22 (474 MB/s) - 'level1.py' saved [876/876]

NoeAH-academy@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
--2026-08-27 01:37:49--  https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.40, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc                                        100%[========================================================================================================================================>]      30  --.-KB/s    in 0s      

2026-08-27 01:37:49 (10.1 MB/s) - 'level1.flag.txt.enc' saved [30/30]

NoeAH-academy@webshell:~$ nano level1.
NoeAH-academy@webshell:~$ nano level1.py
NoeAH-academy@webshell:~$ python3 level1.py
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
```

## Notas adicionales

Revisar el código en Python y analizar su lógica para identificar de dónde se obtiene la contraseña necesaria para mostrar la bandera.

## Referencias