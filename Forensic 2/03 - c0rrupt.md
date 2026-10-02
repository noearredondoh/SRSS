## Descripción

We found this [file](https://challenge-files.cylabacademy.net/library/8388ecc430588d15064755583476bec46e23d42a6d8de6e8995c19e40f2e4c58/c0rrupt-mystery). Recover the flag

- Try fixing the file header
## Solución

```
Para resolver el reto se descargó el archivo proporcionado y se analizó su contenido para identificar por qué no podía abrirse correctamente. La pista indicaba que el problema se encontraba en el header (encabezado) del archivo, por lo que se revisaron sus primeros bytes utilizando herramientas como xxd o un editor hexadecimal. Al comparar la firma encontrada con la estructura correcta del tipo de archivo, se observó que algunos bytes del encabezado habían sido modificados o estaban corruptos. Se reemplazaron estos valores por los correspondientes a una cabecera válida y se guardó el archivo corregido. Después de reparar el encabezado, el sistema pudo reconocer y abrir correctamente el archivo, permitiendo visualizar su contenido y finalmente obtener la flag del reto.
```

```
academy{c0rrupt10n_1847995}
```

## Notas adicionales

## Referencias