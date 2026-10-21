## Descripción

How about some hide and seek?

Download this file [here](https://challenge-files.cylabacademy.net/library/9b029ae1f6eeb888f00d61f70ef1223afce75f409a25b0076838b9af310b66c3/unknown.zip)

1. How can you view the information about the picture?
2. If something isn't in the expected form, maybe it deserves attention?

## Solución

Se descargó y descomprimió el archivo `unknown.zip`, obteniendo la imagen `ukn_reality.jpg`. Posteriormente, se analizaron sus metadatos utilizando el comando:

```
exiftool ukn_reality.jpg
```

e identificó una cadena codificada en Base64 dentro del campo `Attribution URL`. Para recuperar la información oculta, se ejecutó:

```
exiftool -b -AttributionURL ukn_reality.jpg | base64 -d
```

Al decodificar la cadena, se obtuvo la bandera del reto.
```
academy{ME74D47A_HIDD3N_927183b3}
```
## Notas adicionales

## Referencias