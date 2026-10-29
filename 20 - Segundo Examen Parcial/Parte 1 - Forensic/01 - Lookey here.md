## Descripción

Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it. Download the data [here](https://challenge-files.cylabacademy.net/library/764d21f0248d7c1df55583eb1ad863dad241f86f90dd2717e8aa5b9fc3a7e26e/anthem.flag.txt)

1. Download the file and search for the flag based on the known prefix.
## Solución

Para encontrar la bandera en el archivo que descargaste, debes usar el comando `grep` apuntando directamente a `anthem.flag.txt`.

**Paso 1: Abrir la terminal** Abre tu terminal y navega hasta la carpeta exacta donde guardaste el archivo `anthem.flag.txt`.

**Paso 2: Ejecutar la búsqueda** Como el archivo es un texto extenso, utiliza `grep` para filtrar únicamente la línea que contiene el prefijo de la bandera. Ejecuta este comando exacto:

grep "academy{" anthem.flag.txt

```
academy{gr3p_15_@w3s0m3_c16b6693}
```

## Notas adicionales

## Referencias