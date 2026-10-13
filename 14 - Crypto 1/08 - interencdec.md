## Descripción

Can you get the real meaning from this file.

Download the file [here](https://challenge-files.cylabacademy.net/library/0d5754d51dc425dbb46c76eef33bb2b596a1a3bc6f4163ddd2a215f7e0d45198/enc_flag)

## Solución

Primero, descargamos el archivo `enc_flag` y visualizamos su contenido mediante el comando `cat enc_flag`, identificando una cadena codificada en **Base64**.

Posteriormente, ejecutamos `base64 -d enc_flag` para decodificar la primera capa. El resultado contenía otra cadena en Base64, por lo que utilizamos Python para realizar una segunda decodificación.

Después, identificamos que el mensaje resultante estaba cifrado mediante **César**. Probamos los diferentes desplazamientos y encontramos que, al aplicar un desplazamiento de **7 posiciones hacia atrás (ROT19)**, se obtenía la bandera original.

Finalmente, recuperamos la bandera del reto:
```
academy{caesar_d3cr9pt3d_81ed9f02}
```

## Notas adicionales

## Referencias