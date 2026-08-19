## Descripcion
This file has a flag in plain sight (aka "in-the-clear").

## Solucion
```
NoeAH-academy@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/1a44abd1b8ea719b212d4645d5e9805a9db2e9062845609829d5d15e8e7d578c/flag
--2026-08-19 17:07:19--  https://challenge-files.picoctf.net/c_wily_courier/1a44abd1b8ea719b212d4645d5e9805a9db2e9062845609829d5d15e8e7d578c/flag
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.64, 3.160.5.40, 3.160.5.95, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag                                                       100%[========================================================================================================================================>]      34  --.-KB/s    in 0s      

2026-08-19 17:07:19 (15.6 MB/s) - 'flag' saved [34/34]

NoeAH-academy@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_9b8fa0bc}
NoeAH-academy@webshell:~$ 
```

```
picoCTF{s4n1ty_v3r1f13d_9b8fa0bc}
```

## Notas adicionales
Bajar el archivo a la consola y hacer un cat flag

## Referencias
https://webshell.cylabacademy.org/