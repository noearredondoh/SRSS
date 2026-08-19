## Descripcion

If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

## Solucion 1

- Ir al sitio web rapidtables

picoCTF{p}

## Solucion 2
- Ir al interprete de pyhton y teclear los comandos
```
NoeAH-academy@webshell:~$ python
Python 3.10.12 (main, Mar  3 2026, 11:56:32) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> int(0x70)
112
>>> chr(112)
'p'
>>> 
```
## Notas adicionales
- Siempre hay que tener en cuenta el formato de la bandera para que

## Referencias

https://www.rapidtables.com/convert/number/hex-to-ascii.html