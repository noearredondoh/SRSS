## Descripción

I found this cipher in an old book.

## Solución

Primero, nos conectamos al servidor mediante `nc` y guardamos el mensaje cifrado en `cifrado.txt`. Posteriormente, realizamos un análisis de frecuencia con Python utilizando `analizar.py`, donde identificamos que la posible clave era **FLAG**.

Para comprobarlo, utilizamos la página dcode, seleccionamos el cifrado Vigenère e introdujimos la clave `FLAG`, obteniendo un mensaje legible en inglés.

Después, utilizamos el programa `descifrar.py` para descifrar el archivo y extraer la bandera mediante el comando:
```
python3 descifrar.py | grep -oE 'academy\{[^}]+\}'`
```

Finalmente, obtuvimos la bandera:

```
academy{b311a50_0r_v1gn3r3_c1ph3rbb955b0a}
```
## Notas adicionales

El **cifrado de Vigenère** es un método de cifrado polialfabético que utiliza una palabra clave para aplicar diferentes desplazamientos a las letras del mensaje. A diferencia del cifrado César, que emplea un único desplazamiento, Vigenère utiliza varios desplazamientos determinados por la clave.
## Referencias

https://www.dcode.fr/vigenere-cipher