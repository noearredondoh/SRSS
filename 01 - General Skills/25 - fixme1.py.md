## Descripcion

Fix the syntax error in this Python script to print the flag.

[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)

## Solucion

```
NoeAH-academy@webshell:~$ wget https://artifacts.picoctf.net/c/26/fixme1.py
--2026-08-27 01:04:32--  https://artifacts.picoctf.net/c/26/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.40, 3.160.5.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

fixme1.py                                                  100%[========================================================================================================================================>]     837  --.-KB/s    in 0s      

2026-08-27 01:04:33 (396 MB/s) - 'fixme1.py' saved [837/837]

NoeAH-academy@webshell:~$ python3 fixme1.py
  File "/home/NoeAH-academy/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
NoeAH-academy@webshell:~$ nano fixme1.py
NoeAH-academy@webshell:~$ python3 fixme1.py
  File "/home/NoeAH-academy/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
NoeAH-academy@webshell:~$ nano fixme1.py
NoeAH-academy@webshell:~$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}
NoeAH-academy@webshell:~$ 

> Editamos el archivo y le corregimos el error de la linea 20, y volvemos a ejecutar
```

## Notas adicionales

- Los scripst o programas de python pueden no ejecutarse correctamente debido a errores de sintaxis
- nano -l abre el archivo en el editor y muestra los numeros de linea

## Referencias