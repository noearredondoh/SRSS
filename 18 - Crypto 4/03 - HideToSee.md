## Descripción

How about some hide and seek heh? Look at this image [here](https://challenge-files.cylabacademy.net/library/d1a6b6365f32679d90a52e42234c7bad12bdfb9ac5e87598af9f1202ee047227/atbash.jpg)

## Solución

- Se descargó la imagen `atbash.jpg`, la cual contenía información oculta.

- Se analizaron las pistas del reto, identificando que era necesario extraer un archivo oculto dentro de la imagen.

- Se utilizó la herramienta **steghide** mediante el comando `steghide extract -sf atbash.jpg`, dejando la contraseña vacía.

- La extracción permitió obtener el archivo `encrypted.txt`, el cual contenía un mensaje cifrado.

- Se visualizó su contenido mediante el comando `cat encrypted.txt` y se identificó que utilizaba el **cifrado Atbash**.

- Se utilizó el comando `tr` de Linux para sustituir cada letra por su opuesta en el alfabeto, conservando los números y símbolos.

- Finalmente, se obtuvo el mensaje descifrado y se identificó la bandera del reto.
```
academy{atbash_crack_02f11bb3}
```

## Notas adicionales

**Steghide:** Es una herramienta de esteganografía que permite ocultar y extraer información dentro de archivos multimedia, como imágenes y archivos de audio.

**Cifrado Atbash:** Es un método de sustitución monoalfabética que reemplaza cada letra por su opuesta en el alfabeto. Por ejemplo, A se convierte en Z, B en Y y C en X.

**Comando** `**tr**`**:** Es una herramienta de Linux que permite sustituir o eliminar caracteres de un texto. En este reto se utilizó para realizar el descifrado Atbash.

## Referencias