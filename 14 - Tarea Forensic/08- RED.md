## Descripción

RED, RED, RED, RED Download the image: [red.png](https://challenge-files.cylabacademy.net/library/fefcf06050d98347e1585e5cb9f2940967f82e0b89c591966473c752de9f3aba/red.png)

## Solución

Se descargó la imagen `red.png` y se analizaron sus metadatos utilizando `exiftool`. Posteriormente, se empleó la herramienta `zsteg` para buscar información oculta en los canales de color.

```
zsteg red.png
```

Se identificó una cadena codificada en Base64 mediante la técnica de esteganografía LSB. Para extraerla y decodificarla se ejecutó:

```
zsteg -E 'b1,rgba,lsb,xy' red.png | base64 -d
```

Como resultado, se obtuvo la bandera repetida varias veces, de la cual se extrajo una sola copia.

```
academy{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}
```

## Notas adicionales

`zsteg` es una herramienta de análisis forense que permite detectar información oculta en imágenes PNG y BMP, examinando los bits menos significativos de sus canales de color (RGBA).

## Referencias