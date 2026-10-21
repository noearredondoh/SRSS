## Descripción

Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://challenge-files.cylabacademy.net/library/c585b4adbdaa06f409db7bf5012c2e58e9aab24669764a5f1cf0f9ce0d60dcfd/cat.jpg)

1. Look at the details of the file
2. Make sure to submit the flag as academy{XXXXX}

## Solución

Se descargó el archivo `cat.jpg` y se analizaron sus metadatos utilizando la herramienta `exiftool`. Durante el análisis se identificó una cadena codificada en Base64 dentro del campo `License`. Posteriormente, se utilizó el comando:
```
exiftool -b -License cat.jpg | base64 -d
```


Al decodificar la cadena, se obtuvo la bandera del reto:
```
academy{the_m3tadata_1s_modified}
```

## Notas adicionales

## Referencias