## Descripcion

Fix the syntax error in the Python script to print the flag.

[Download Python script](https://artifacts.picoctf.net/c/5/fixme2.py)

## Solucion

```
NoeAH-academy@webshell:~$ wget https://artifacts.picoctf.net/c/5/fixme2.py
--2026-08-27 01:26:33--  https://artifacts.picoctf.net/c/5/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.40, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                                                  100%[========================================================================================================================================>]   1.00K  --.-KB/s    in 0s      

2026-08-27 01:26:33 (453 MB/s) - 'fixme2.py' saved [1029/1029]

NoeAH-academy@webshell:~$ python3 fixme2.py
  File "/home/NoeAH-academy/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?

>> Hay que corregir el error

NoeAH-academy@webshell:~$ nano -l fixme2.py
NoeAH-academy@webshell:~$ python3 fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}
```

## Notas adicionales

## Referencias