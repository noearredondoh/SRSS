## Descripción

This file seems broken... or is it? Maybe a couple of bytes could make all the difference. Can you figure out how to bring it back to life? Download the file [here](https://challenge-files.cylabacademy.net/library/03e658f970a580c265471fa9e2477a66457bed10e5f89da0fe70c141c3509f3b/file)

1. Try checking the file’s header.
2. JPEG
3. Tools like xxd or hexdump can help you inspect and edit file bytes.
## Solución

1. Se descargó el archivo llamado `file` y se analizó mediante el comando `file file`, identificando que el sistema no reconocía su formato.

2. Se utilizó el comando `xxd -l 32 file` para examinar los primeros 32 bytes del archivo en hexadecimal.

3. Se identificó que los primeros bytes eran `5C 78`, cuando la firma correcta de una imagen JPEG debe comenzar con `FF D8`.

4. Se creó una copia del archivo original mediante el comando `cp file imagen.jpg`.

5. Se reparó la cabecera utilizando el siguiente comando:

    `printf '\xFF\xD8' | dd of=imagen.jpg bs=1 seek=0 count=2 conv=notrunc`

6. Se verificó la reparación mediante `file imagen.jpg`, confirmando que el sistema reconocía correctamente el formato JPEG.

7. Se abrió la imagen con `xdg-open imagen.jpg` y se identificó la bandera escrita en su interior.

8. Finalmente, se amplió la imagen para comprobar los caracteres y obtener la bandera correcta.
```
academy{r3st0r1ng_th3_by73s_69066302}`
```
## Notas adicionales

**Cabecera de archivo:** Es una sección inicial que contiene información utilizada para identificar el formato y la estructura de un archivo.

**Magic Bytes:** Son secuencias de bytes características que permiten identificar un formato. En JPEG, la firma comienza con `FF D8 FF`.

## Referencias