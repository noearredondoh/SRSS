## Descripción

I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?

You can download the challenge files here:

- [challenge.zip](https://challenge-files.cylabacademy.net/library/2ec57d777f5f27f3b32ce12fb8437359ea4c9b6429f8adaf6f7d428653adc865/challenge.zip)
## Solución

Se descargó y descomprimió el archivo `challenge.zip`, encontrando una imagen llamada `flag.png` dentro de la carpeta `home/ctf-player/drop-in`.

Posteriormente, se utilizó la herramienta `zbarimg` para analizar el código QR contenido en la imagen mediante el comando

```
zbarimg home/ctf-player/drop-in/flag.png
```

Al decodificar el código QR, se obtuvo directamente la bandera del reto.
```
academy{p33k_@_b00_ebb7f3f7}
```
## Notas adicionales

`zbar-tools` es un conjunto de herramientas que permite leer y decodificar códigos de barras y códigos QR. Incluye el comando `zbarimg`, útil en análisis forenses para extraer información almacenada en imágenes.
## Referencias