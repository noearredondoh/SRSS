## Descripción

It seems that another encrypted message has been intercepted. The encryptor seems to have learned their lesson though and now there isn't any punctuation! Can you still crack the cipher? Download the message [here](https://challenge-files.cylabacademy.net/library/750a77d87fa924d5ec8a173d7354dd57792a1597cab3d89fa7443608ba0a35e7/message.txt).
## Solución

1. Se descargó el archivo `message.txt` y se visualizó su contenido mediante el comando `cat message.txt`.

2. Se identificó que el mensaje utilizaba un cifrado por sustitución monoalfabética sin separaciones entre palabras.

3. Se utilizó la herramienta **Quipqiup** para realizar un análisis de frecuencias y obtener una primera aproximación del mensaje original.

4. Se seleccionó el resultado más coherente en inglés, aunque algunas letras todavía no se habían descifrado correctamente.

5. Se creó un script en Python llamado `solve.py` para reconstruir la tabla de sustitución utilizando fragmentos conocidos del mensaje.

6. Se analizaron las correspondencias entre caracteres y se identificaron las letras que faltaban mediante el script.

7. Se completó la sustitución restante y se recuperó la bandera, que posteriormente fue aceptada por la plataforma.

```
academy{N6R4M_4N41Y515_15_73D10U5_FD56C357}
```

## Notas adicionales

## Referencias
https://quipqiup.com/