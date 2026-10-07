## Descripción

Download this disk image and find the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://challenge-files.cylabacademy.net/library/135adeee1de1ceb2e2838061773078678e93ff1d16535b39a17481b2ba5868ff/disk.flag.img.gz)

## Solución

Se descargó y descomprimió la imagen de disco proporcionada por el reto dentro del directorio `/tmp`. Posteriormente, se utilizó `mmls` para identificar las particiones existentes:
```
mmls disk.flag.img
```

Se identificó que la partición principal de Linux comenzaba en el sector **360448**. Para visualizar su contenido se utilizó:
```
fls -o 360448 disk.flag.img
```

Después, se realizó una búsqueda recursiva para localizar archivos relacionados con la bandera:
```
fls -r -o 360448 disk.flag.img | grep -i flag
```

La búsqueda mostró los archivos `flag.txt` y `flag.uni.txt`. Este último se encontraba asociado al inode **2371**, por lo que se utilizó `icat` para recuperar directamente su contenido:
```
icat -o 360448 disk.flag.img 2371
```

Al ejecutar el comando se mostró el contenido de `flag.uni.txt`, obteniendo así la bandera y completando el reto.

```
academy{by73_5urf3r_217f681f}
```

## Notas adicionales

## Referencias