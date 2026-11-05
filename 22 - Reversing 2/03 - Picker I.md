## Descripción

This service can provide you with a random number, but can it do anything else?
## Solución

1. Se descargó y analizó el código fuente del programa, identificando las funciones `getRandomNumber()` y `win()`.

2. Se observó que el programa utilizaba `eval()` para ejecutar la función introducida por el usuario:
    ```python
    user_input = input("==> ")
    eval(user_input + '()')
    ```

3. Se estableció una conexión con el servidor 

4. Cuando el programa solicitó una función, se introdujo:
    ```text
    win
    ```
    Esto permitió ejecutar `win()`, que mostró la bandera codificada en hexadecimal.
    
5. Se convirtió la secuencia hexadecimal a texto ASCII utilizando Python:
    ```bash
    python3 -c "print(bytes.fromhex('61636164656d797b345f6431346d306e645f316e5f3768335f72307567685f33333938343138387d').decode())"
    ```
    Finalmente, se recuperó la bandera original.
```
academy{4_d14m0nd_1n_7h3_r0ugh_33984188}
```
## Notas adicionales

## Referencias