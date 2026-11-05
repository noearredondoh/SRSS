## Descripción

Can you figure out how this program works to get the flag?
## Solución

1. Se descargaron los archivos `picker-IV` y `picker-IV.c`, correspondientes al ejecutable y su código fuente.

2. Se utilizó el comando `nm` para localizar la dirección de memoria de la función `win()`:
    ```bash
    nm picker-IV | grep ' win'
    ```
    Se obtuvo el siguiente resultado:
    ```text
    00000000004012a1 T win
    ```

3. Se analizó el código fuente mediante:
    ```bash
    cat picker-IV.c
    ```
    Se identificó que el programa utilizaba `scanf("%x", &val)` para recibir una dirección hexadecimal y ejecutarla mediante un puntero a función.

4. Se estableció una conexión con el servidor.

5. Cuando el programa solicitó una dirección de memoria, se introdujo:
    ```text
    4012a1
    ```
    Esto permitió ejecutar la función `win()`, que abrió el archivo `flag.txt` y mostró la bandera.
```
academy{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_cd521e4c}
```
## Notas adicionales

**Binary Exploitation:** Técnica que aprovecha vulnerabilidades en programas compilados para modificar su comportamiento.
## Referencias