## Descripcion
Our flag printing service has started glitching!
## Solucion
```
NoeAH-academy@webshell:~$ nc saturn.picoctf.net 61998
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
^C
NoeAH-academy@webshell:~$ python
Python 3.10.12 (main, Mar  3 2026, 11:56:32) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
'picoCTF{gl17ch_m3_n07_9c42a45d}'
>>> 
```

```
picoCTF{gl17ch_m3_n07_9c42a45d}
```

## Notas adicionales
Abrir el puerto del servidor y mandara la bandera, pero sin teriminar y con ayuda de python traducimos la bandera.

## Referencias
https://webshell.cylabacademy.org/