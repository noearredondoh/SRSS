## Descripción

The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?

Download the suspicious file [here](https://challenge-files.cylabacademy.net/library/fbc63a04a60481fd928460868dee05e60ab0bcdf6582dc786ddf1f1cec3f8c8b/flag2of2-final.pdf)

## Solución

Se descargó el archivo `flag2of2-final.pdf` y se analizó utilizando el comando:
```
file flag2of2-final.pdf
```

Se identificó que, aunque tenía extensión PDF, también podía interpretarse como una imagen PNG. Se creó una copia con extensión `.png`:
```
cp flag2of2-final.pdf flag.png
```

Posteriormente, se abrió la imagen con Firefox, encontrando la primera parte de la bandera. Finalmente, se abrió el archivo original como PDF, obteniendo la segunda parte. Al unir ambas cadenas, se recuperó la bandera completa

```
academy{f1u3n7_1n_pn9_&_pdf_96385309}
```

## Notas adicionales

Un archivo políglota es aquel que puede interpretarse en diferentes formatos. Esta técnica permite almacenar información de distintos tipos dentro de un mismo archivo y es útil en retos de análisis forense digital.

## Referencias