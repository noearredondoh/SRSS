## Descripción

A message has come in but it seems to be all scrambled. Luckily it seems to have the key at the beginning. Can you crack this substitution cipher? Download the message [here](https://challenge-files.cylabacademy.net/library/c81cd186dacb4ad82560df3b81fe365fc1c38a1c7dca9a73a9604c5345ab4473/message.txt).

## Solución

1. Se descargó el archivo `message.txt`, que contenía un mensaje cifrado y la clave de sustitución.

2. Se visualizó su contenido mediante el comando `cat message.txt`, identificando la clave `DJHMILABFORYVGNKUXQSCPEWZT`.

3. Se creó un script en Python llamado `solve.py` para automatizar el descifrado.

4. Se utilizó la función `str.maketrans()` para construir una tabla que relacionara las letras cifradas con las letras originales del alfabeto.

5. Se aplicó el método `translate()` para sustituir los caracteres y recuperar el mensaje original.

6. Finalmente, se ejecutó el script mediante `python3 solve.py`, obteniendo la bandera del reto.
```
academy{5UB5717U710N_3V0LU710N_6A8C4822}
```

## Notas adicionales

**Cifrado por sustitución monoalfabética:** Es un método de criptografía clásica que reemplaza cada letra del alfabeto por otra siguiendo una clave fija. Para descifrarlo se utiliza la correspondencia inversa.

## Referencias