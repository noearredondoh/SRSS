## Descripción

Can you figure out how this program works to get the flag?
## Solución

1. Se descargó el archivo `picker-III.py` y se analizaron las funciones del programa:
    ```bash
    grep -nE 'def |func_table|win|eval|exec' picker-III.py
    ```

2. Se identificó la variable `func_table`, que almacenaba cuatro funciones, y el método `write_variable()`, que permitía modificar su contenido.

3. Se estableció una conexión con el servidor 

4. Se seleccionó la opción `3` para ejecutar `write_variable()`. Cuando solicitó el nombre de la variable, se introdujo:
    ```text
    func_table
    ```

5. Se modificó la tabla introduciendo la siguiente expresión:
    ```python
    'win' + ' '*125
    ```
    Esto reemplazó la primera función por `win`, conservando los 128 caracteres requeridos por el programa.
    
6. Se seleccionó la opción `1`, ejecutando la función `win()`, que mostró la bandera codificada en hexadecimal.

7. Finalmente, se convirtió la secuencia hexadecimal a texto ASCII para recuperar la bandera original.
```
academy{7h15_15_wh47_w3_g37_w17h_u53r5_1n_ch4rg3_948e866e}
```
## Notas adicionales

## Referencias
https://gchq.github.io/CyberChef/