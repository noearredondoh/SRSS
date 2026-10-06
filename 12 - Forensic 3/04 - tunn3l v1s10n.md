## Descripción

We found this file. Recover the flag. [tunn3l_v1s10n](https://challenge-files.cylabacademy.net/library/3b5add918cb4cf98fa62ef4e05eb8c55c6c9ae547a939c6be992ee3aa656ee69/tunn3l_v1s10n)

- Weird that it won't display right...

## Solución

Se descargó el archivo `tunn3l_v1s10n`, el cual no contaba con una extensión que permitiera identificar directamente su formato. Al analizar los primeros bytes del archivo se encontró la firma hexadecimal `42 4D`, correspondiente a una imagen en formato BMP.

Al intentar abrir la imagen se presentó un error, por lo que se utilizó un editor hexadecimal para revisar su cabecera. Durante el análisis se identificaron valores modificados que impedían que el archivo fuera interpretado correctamente. Para reparar la imagen, se modificó el offset `0x0A`, estableciendo el valor `36 00 00 00`, correspondiente a 54 bytes para indicar el inicio de los datos de los píxeles. También se corrigió el offset `0x0E` con el valor `28 00 00 00`, correspondiente a una cabecera DIB de 40 bytes.

Después de realizar estas modificaciones, la imagen pudo visualizarse correctamente; sin embargo, únicamente mostraba un paisaje acompañado del texto **“NOT THE FLAG”**. Tomando como referencia el nombre del reto, `tunn3l_v1s10n` (“tunnel vision”), se determinó que probablemente existía información fuera del área visible de la imagen.

Se volvió a analizar la cabecera del archivo y se modificó el valor correspondiente a la altura de la imagen, ubicado en el offset `0x16`, cambiándolo de `32 01` a `32 03`. Con este cambio se amplió el área vertical que el visor debía mostrar, revelando una sección de la imagen que anteriormente permanecía oculta.

Finalmente, debido a las dimensiones poco comunes de la imagen, algunos visores de Linux no mostraban correctamente todo el contenido. Por esta razón, se abrió el archivo mediante Firefox o se utilizó ImageMagick para visualizarlo con un tamaño adecuado. De esta manera fue posible observar completamente el área oculta y obtener la bandera del reto.

```
academy{qu1t3_a_v13w_2020}
```

## Notas adicionales

## Referencias