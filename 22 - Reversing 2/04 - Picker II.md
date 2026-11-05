## Descripción

Can you figure out how this program works to get the flag?

## Solución

1. Se descargó y analizó el código fuente del programa, identificando la función `win()`, encargada de leer y mostrar la bandera.

2. Dentro de la función `win()` se encontró la siguiente instrucción:
    ```python
    flag = open('flag.txt', 'r').read()
    ```
    Esto permitió identificar que la bandera estaba almacenada en el archivo `flag.txt`.

3. Se estableció una conexión con el servidor 

4. Se aprovechó la evaluación de expresiones del programa introduciendo:
    ```python
    print(open('flag.txt', 'r').read())
    ```
    Esta instrucción permitió leer directamente el archivo que contenía la bandera.

5. El servidor mostró la bandera junto con un error `NoneType`, debido a que el programa intentó llamar como función al resultado de `print()`. Sin embargo, la bandera ya había sido recuperada.
```
academy{f1l3r35_f4l1_c0d3_r3f4c70r_n1gh7_5ucc33d_e9683452}
```
## Notas adicionales

## Referencias