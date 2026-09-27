## Descripción

Can you get the flag? Go to this [website](http://chatelaine.cylabacademy.net:17847/) and see what you can discover.

## Solución

```
Se reviso el código HTML de la página y encontramos que cargaba dos archivos externos:

<link rel="stylesheet" href="style.css">
<script src="script.js"></script>

Revisé el archivo style.css y encontré la primera parte de la bandera.

Después revisé script.js, donde se encontraba la segunda parte.

Finalmente, uní ambas partes para obtener la bandera completa:
```

```
academy{1nclu51v17y_1of2_f7w_2of2_64d6df37}
```

## Notas adicionales

## Referencias