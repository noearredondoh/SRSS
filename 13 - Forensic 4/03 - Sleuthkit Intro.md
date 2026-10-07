## Descripción

Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

[Download disk image](https://challenge-files.cylabacademy.net/library/d8718cbbc14dcd9f9aad532a51d7a01b00e1715ca3b1d654dfef687d0b15cbf5/disk.img.gz)

## Solución

Se descargó la imagen de disco proporcionada por el reto y se descomprimió dentro del directorio `/tmp`, tal como indicaban las instrucciones.

Posteriormente, se utilizó la herramienta `mmls` de **The Sleuth Kit** para visualizar la tabla de particiones de la imagen:
```
mmls disk.img
```

En la salida se identificó la partición correspondiente a **Linux** y se tomó el valor mostrado en la columna `Length`, que representa su tamaño en sectores.

Finalmente, se realizó la conexión con el servidor de verificación mediante:
```
nc xebec.cylabacademy.net 45386
```

Cuando el servidor solicitó el tamaño de la partición Linux, se introdujo el valor obtenido con `mmls`, obteniendo así la bandera del reto.
```
academy{mm15_f7w!}
```

## Notas adicionales

La herramienta `mmls` permite visualizar la estructura de particiones de una imagen de disco, mostrando datos como el sector inicial, sector final, longitud y tipo de cada partición.
## Referencias