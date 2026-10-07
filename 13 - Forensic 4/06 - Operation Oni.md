## Descripción

Download this disk image, find the key and log into the remote machine.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

## Solución

Se descargó y descomprimió la imagen de disco proporcionada por el reto. Posteriormente, se utilizó `mmls` para analizar su tabla de particiones:
```
mmls disk.img
```

Listamos los archivos del sistema de forma recursiva en esa partición buscando la clave SSH de root:
```
fls -o 206848 -r disk.img | grep -i "id_"
```
Localizamos el archivo de la clave privada `id_ed25519` asociado al inode **`2345`**

Extraemos el contenido de la clave privada a un archivo local utilizando `icat`:
```
icat -o 206848 disk.img 2345 > key_file
```

Asignamos permisos restrictivos de lectura al archivo de la clave:
```
chmod 600 key_file
```

Nos conectamos vía SSH al servidor remoto especificando el puerto y la clave recién extraída:
```
ssh -i key_file -p 38546 ctf-player@chatelaine.cylabacademy.net
```

Una vez dentro de la sesión remota, leemos la bandera guardada en el directorio principal:
```
cat flag.txt
```

Y encontamos la bandera
```
academy{k3y_5l3u7h_0e000cd7}
```

## Notas adicionales

## Referencias

https://gemini.google.com/app?hl=es
