## Descripción

A type of transposition cipher is the rail fence cipher, which is described [here](https://en.wikipedia.org/wiki/Rail_fence_cipher). Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it? Download the message [here](https://challenge-files.cylabacademy.net/library/54f070d7a4fbb401b7ae06e5f41a3071cc195039368a58d9c6bb6f5a95b7913c/message.txt)
The decoded message names a phrase. Put that phrase, and nothing else, in the academy flag format: `academy{phrase}`.

## Solución

1. Se descargó el archivo `message.txt`, que contenía el mensaje cifrado.

2. Se identificó que el mensaje utilizaba el cifrado Rail Fence con 4 rieles, según las instrucciones del reto.

3. Se creó un script en Python llamado `rail.py` para automatizar el descifrado.

4. Se implementó un algoritmo que reconstruye las posiciones originales de los caracteres siguiendo un patrón de zigzag.

5. Se ejecutó el script mediante el comando `python3 rail.py`.

6. Finalmente, se obtuvo el mensaje descifrado y se extrajo la frase para formar la bandera solicitada.
```
academy{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_8CEF1166}
```
## Notas adicionales

**Rail Fence:** Es un cifrado de transposición que reorganiza los caracteres de un mensaje en varias filas o rieles siguiendo un patrón de zigzag. Para descifrarlo, se reconstruye el recorrido original de los caracteres.

## Referencias

https://en.wikipedia.org/wiki/Rail_fence_cipher