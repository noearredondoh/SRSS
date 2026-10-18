## Descripción

The numbers... what do they mean? [numbers](https://challenge-files.cylabacademy.net/library/664bc3a85525cfd5a2af151d29f2744ba334880e28e60f9a513aba13633199d4/the_numbers.png)

## Solución

Se descargó la imagen proporcionada por el reto, en la cual aparecía una secuencia de números. Al analizarla, se identificó que correspondía al cifrado **A1Z26**, donde cada número representa una letra del abecedario (1=A, 2=B, ..., 26=Z).

Para descifrar el mensaje, se utilizó Python desde la terminal de Kali Linux, ejecutando el siguiente código:

```python
numeros = [16,9,3,15,3,20,6,20,8,5,14,21,13,2,5,18,19,13,1,19,15,14]
mensaje = ''.join(chr(n + 64) for n in numeros)
print(mensaje)
```

El código convirtió los números en sus letras correspondientes mediante la función `chr()`, obteniendo el mensaje `PICOCTFTHENUMBERSMASON`. Finalmente, se colocó el contenido descifrado en el formato solicitado por picoCTF, obteniendo la bandera:

```
picoCTF{THENUMBERSMASON}
```

## Notas adicionales

## Referencias