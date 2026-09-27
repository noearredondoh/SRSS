## Descripción

How about trying to match a regular expression

http://saturn.picoctf.net:50213/
## Solución

- Se accedió al enlace de la aplicación web del reto (`[http://saturn.picoctf.net:50213/](http://saturn.picoctf.net:50213/)`).

- Se inspeccionó el código fuente de la página web mediante las Herramientas de Desarrollador del navegador (o presionando `Ctrl + U` / `F12`).

- En el script de JavaScript ejecutable de la página, se identificó la función que valida la entrada del usuario mediante la expresión regular `^picoCTF{.*}`.

-  ingresó una cadena que coincidiera con el patrón requerido por la Expresión Regular para activar la respuesta del servidor o revelar la bandera.

```
picoCTF{succ3ssfully_matchtheregex_0694f2b5}
```

## Notas adicionales

## Referencias

