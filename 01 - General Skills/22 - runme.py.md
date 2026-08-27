## Descripcion

Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.

[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)

## Solucion

```
NoeAH-academy@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2026-08-26 16:20:36--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.40, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py                                                   100%[========================================================================================================================================>]     270  --.-KB/s    in 0s      

2026-08-26 16:20:36 (58.1 MB/s) - 'runme.py' saved [270/270]

NoeAH-academy@webshell:~$ python3 runme.py
picoCTF{run_s4n1ty_run}
```

```
picoCTF{run_s4n1ty_run}
```

## Notas adicionales

- Para ejecutar un script de python simplemente: python3.script.py

## Referencias