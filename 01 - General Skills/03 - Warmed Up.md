## Descripcion
What is 0x3D (base 16) in decimal (base 10)?

## Solucion
```
NoeAH-academy@webshell:~$ python
Python 3.10.12 (main, Mar  3 2026, 11:56:32) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> int("0x30",16)
48
>>> int("0x3D,16)
  File "<stdin>", line 1
    int("0x3D,16)
        ^
SyntaxError: unterminated string literal (detected at line 1)
>>> int ("0X3D",16)
61
>>> 
```
picoCTF{61}
## Notas adicionales
Las funciones int, convierte cualquier numero a base 10, el segundo parametro indica la base en la que esta el numero

## Referencias
https://webshell.cylabacademy.org/