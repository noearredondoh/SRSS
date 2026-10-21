## Descripción

Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://challenge-files.cylabacademy.net/library/f7b0490c7122b66d8882c3da0c6b027eab5a9ffa3ea6b5e4c903bc3f30a950aa/flag.png)

## Solución

Se descargó el archivo `flag.png` y se analizó utilizando la herramienta `binwalk` para identificar archivos ocultos en su interior.

```
binwalk flag.png
```

Se detectó un archivo ZIP incrustado que contenía una carpeta llamada `secret`. Posteriormente, se extrajo su contenido mediante:

```
binwalk -e flag.png
```

Finalmente, se abrió la imagen oculta utilizando:

```
xdg-open _flag.png.extracted/secret/flag.png
```

Al visualizar la imagen extraída, se encontró la bandera del reto:

```
academy{Hiddinng_An_imag3_within_@n_ima9e_404ff71e}
```

## Notas adicionales

`binwalk` es una herramienta de análisis forense que permite detectar y extraer archivos incrustados dentro de otros archivos, como imágenes, documentos y firmware. Es especialmente útil para identificar información oculta mediante técnicas de esteganografía.
## Referencias