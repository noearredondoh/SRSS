## Descripción

I have these 2 images, can you make a flag out of them? [scrambled1.png](https://challenge-files.cylabacademy.net/library/c9d53b01e497af3b9886cf52c7896ec4b26d82dd88402905e13258cbbbe82b21/scrambled1.png) [scrambled2.png](https://challenge-files.cylabacademy.net/library/c9d53b01e497af3b9886cf52c7896ec4b26d82dd88402905e13258cbbbe82b21/scrambled2.png)

## Solución

- Se descargaron los archivos `scrambled1.png` y `scrambled2.png`, los cuales contenían imágenes con píxeles aparentemente aleatorios.

- Se analizaron las pistas del reto, identificando que era necesario superponer ambas imágenes para revelar el mensaje oculto.

- Utilizando **Python** y la biblioteca **Pillow**, se combinaron las imágenes mediante `Image.blend()`, aplicando una transparencia del 50 % a cada una.

- Como el texto no era completamente visible, se utilizó `ImageChops.add()` para combinar los píxeles y mejorar el resultado.

- Posteriormente, se convirtió la imagen a escala de grises con `ImageOps.grayscale()` y se aumentó el contraste mediante `ImageOps.autocontrast()`.

- Finalmente, se amplió la imagen para facilitar su lectura, logrando visualizar la bandera oculta.
```
academy{2f16d0c4}
```
## Notas adicionales

**Criptografía visual:** Es una técnica que permite ocultar información dentro de imágenes, de manera que el mensaje original pueda revelarse al superponerlas correctamente.

**Pillow:** Es una biblioteca de Python utilizada para procesar y manipular imágenes. Permite combinar imágenes, modificar sus colores, ajustar el contraste y cambiar su tamaño.

## Referencias

[Visual Cryptography - Wikipedia](https://en.wikipedia.org/wiki/Visual_cryptography)