## Descripción

This file contains more than it seems. Get the flag from [garden.jpg](https://challenge-files.cylabacademy.net/library/e78198c6a7dc5e471e8429d4953e7595feafe17764258eec169b8dab8bb3c925/garden.jpg)

## Solución

```
**Decarga el archivo**
wget https://challenge-files.cylabacademy.net/library/e78198c6a7dc5e471e8429d4953e7595feafe17764258eec169b8dab8bb3c925/garden.jpg

**Extracción de la bandera**
strings -n 10 garden.jpg
strings -n 10 garden.jpg | grep academy
```

```
academy{more_than_m33ts_the_3y3e23d7ba9}
```

## Notas adicionales

Al ejecutar `strings`, analizó los datos binarios de la imagen y filtró las cadenas legibles de texto con 10 o más caracteres. Esto permitió encontrar la _flag_ oculta al final del archivo sin distorsionar el visor.

## Referencias