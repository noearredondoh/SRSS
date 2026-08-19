## Descripcion
What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.

## Solucion
```
NoeAH-academy@webshell:~$ python
Python 3.10.12 (main, Mar  3 2026, 11:56:32) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import base64
>>> base64.b64decode("bDNhcm5fdGgzX3IwcDM1")
b'l3arn_th3_r0p35'
>>> 
```

```
picoCTF{b'l3arn_th3_r0p35'}
```

## Notas adicionales
Abrir el interprete de pytho en cylab e Importar base64 y haciendo uso de esta obtenemos la bandera

## Referencias
https://es.wikipedia.org/wiki/Base64