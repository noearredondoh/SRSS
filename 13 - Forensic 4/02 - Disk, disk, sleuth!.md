## Descripción

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image. [dds1-alpine.flag.img.gz](https://challenge-files.cylabacademy.net/library/cb4d1ac86836c86e1ea16a4be1d8cf72c0465c6edcc0ab886728040a28dd7966/dds1-alpine.flag.img.gz)

## Solución

Se descargó el archivo `dds1-alpine.flag.img.gz` proporcionado por el reto. Posteriormente, se utilizó el comando `file` para identificar su formato, confirmando que se trataba de un archivo comprimido con **gzip**.

El archivo se descomprimió mediante:
```
gunzip dds1-alpine.flag.img.gz
```

Esto generó la imagen de disco `dds1-alpine.flag.img`. Debido a que el reto indicaba el uso de herramientas de **Sleuth Kit**, se utilizó `srch_strings` para buscar cadenas de texto legibles dentro de la imagen y `grep` para filtrar directamente la bandera:

```
srch_strings dds1-alpine.flag.img | grep -i academy
```

```
academy{f0r3ns1c4t0r_n30phyt3_6502313d}
```

## Notas adicionales

`srch_strings` permite buscar cadenas de texto dentro de una imagen de disco, mientras que `grep` facilita localizar únicamente aquellas que coinciden con un patrón específico, como `picoCTF`
## Referencias