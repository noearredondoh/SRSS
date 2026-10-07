## Descripción

Download this disk image and find the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://challenge-files.cylabacademy.net/library/c43b9c25ad2c97fb0c7c393a7b5f95065b79c0faf5848e1eeb6a453ec3e78f7d/disk.flag.img.gz)

## Solución

Se descargó y descomprimió la imagen de disco proporcionada por el reto. Posteriormente, se utilizó `mmls` para analizar su tabla de particiones:
```
mmls disk.flag.img
```

Se identificó que el sistema de archivos principal de Linux comenzaba en el sector **411648**, por lo que se examinó utilizando:
```
fls -o 411648 disk.flag.img
```

Después se realizó una búsqueda recursiva de archivos relacionados con la bandera:
```
fls -r -o 411648 disk.flag.img | grep -i flag
```

Esto permitió localizar `flag.txt` y `flag.txt.enc`. El primero aparecía como un archivo eliminado, mientras que el segundo correspondía a información cifrada. Ambos se recuperaron mediante sus respectivos inodes:
```
icat -o 411648 disk.flag.img 1876 > flag.txt
icat -o 411648 disk.flag.img 1782 > flag.txt.enc
```

Al revisar el directorio `root` se encontró el archivo `.ash_history`. Su contenido se recuperó con:
```
icat -o 411648 disk.flag.img 1875
```

En el historial se encontró el comando utilizado originalmente para cifrar la bandera:
```
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
```

Gracias a esta información se obtuvo tanto el algoritmo utilizado, **AES-256**, como la contraseña. Finalmente, se descifró el archivo:
```
openssl aes256 -d -in flag.txt.enc -out flag_decrypted.txt -k unbreakablepassword1234567
```

Y finalmente obtenemos la bandera

```
academy{h4un71ng_p457_0cf3a06d}
```

## Notas adicionales

## Referencias