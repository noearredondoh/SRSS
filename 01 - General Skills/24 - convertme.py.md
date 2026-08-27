## Descripcion

Run the Python script and convert the given number from decimal to binary to get the flag.

[Download Python script](https://artifacts.picoctf.net/c/23/convertme.py)

## Solucion

```
NoeAH-academy@webshell:~$ wget https://artifacts.picoctf.net/c/23/convertme.py
--2026-08-26 16:28:47--  https://artifacts.picoctf.net/c/23/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.18, 3.160.5.40, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                                               100%[========================================================================================================================================>]   1.16K  --.-KB/s    in 0s      

2026-08-26 16:28:47 (58.0 MB/s) - 'convertme.py' saved [1189/1189]

NoeAH-academy@webshell:~$ pythone convertme.py
-bash: pythone: command not found
NoeAH-academy@webshell:~$ python convertme.py
If 26 is in decimal base, what is it in binary base?
Answer: 11010
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_9c3b7d4d}
```

```
picoCTF{4ll_y0ur_b4535_9c3b7d4d}
```

## Notas adicionales

- https://gchq.github.io/CyberChef/#recipe=To_Base(2)&input=MjY
- Usamos la formula To Base y le pusimos base 2 en CyberChef

## Referencias
https://gchq.github.io/CyberChef/#recipe=To_Base(2)&input=MjY