## Descripción

Morse code is well known. Can you decrypt this? Download the file [here](https://challenge-files.cylabacademy.net/library/3728bfa4e8314fddd6b7e9f3fae9cb453b459a0bd4b3a29a9224701152f0cd89/morse_chal.wav).

Wrap your answer with academy{}, put underscores in place of pauses, and use all uppercase.
## Solución

1. Se descargó el archivo `morse_chal.wav` y se abrió en Audacity para visualizar las señales de audio.

2. Se identificaron los sonidos cortos, largos y las pausas, que representan los elementos del código Morse.

3. Se exportó el audio como `morse_fixed.wav` en formato WAV de 16 bits para facilitar su procesamiento con Python.

4. Se creó un script llamado `morse.py`, utilizando las bibliotecas NumPy y SciPy para analizar las duraciones de los sonidos y silencios.

5. Se identificaron los puntos, rayas y separaciones, guardando la secuencia obtenida en `morse.txt`.

6. Se desarrolló otro script llamado `decodificar.py`, que utilizó un diccionario de código Morse para convertir las señales en letras y números.

7. Finalmente, se generó la bandera utilizando letras mayúsculas y guiones bajos en lugar de espacios.
```
academy{WH47_H47H_90D_W20U9H7}
```

## Notas adicionales

**Código Morse:** Es un sistema de comunicación que representa letras y números mediante combinaciones de señales cortas (puntos) y largas (rayas).

## Referencias