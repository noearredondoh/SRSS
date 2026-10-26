## Descripción

Can you decrypt this message? Decrypt this [message](https://challenge-files.cylabacademy.net/library/7e1288d31bc6645f95d07bcf09caaf93210591ba082ba0f14490f0767ad7fd33/cipher.txt) using this key "CYLAB".
## Solución

1. Se descargó el archivo `cipher.txt`, que contenía el mensaje cifrado.

2. Se visualizó su contenido mediante el comando `cat cipher.txt`.

3. Se identificó que el mensaje utilizaba el cifrado Vigenère y que la clave proporcionada era `CYLAB`.

4. Se creó un script en Python llamado `solve.py` para automatizar el descifrado.

5. Se implementó un algoritmo que aplica desplazamientos inversos a cada letra del mensaje utilizando los valores de la clave.

6. Se conservaron los números, guiones bajos y símbolos sin modificaciones.

7. Finalmente, se ejecutó el script mediante `python3 solve.py`, recuperando el mensaje original y la bandera.
```
academy{DONT_US3_V1G3N3R3_C1PH3R_4a372077}
```

## Notas adicionales

**Cifrado Vigenère:** Es un método de cifrado polialfabético que utiliza una palabra clave para determinar diferentes desplazamientos de las letras del mensaje. Para descifrarlo, se aplican los desplazamientos inversos utilizando la misma clave.

## Referencias
https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher