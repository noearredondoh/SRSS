## Descripción

The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://challenge-files.cylabacademy.net/library/bff045020b5b976b6d28cf9e3d1ac570e8733c96c9d0fbc14bf923b352796348/need-for-speed)

1. What is the final key?

## Solución

1. Descargamos el archivo `need-for-speed` desde la página del reto.

2. Le otorgamos permisos de ejecución y lo ejecutamos:
    ```bash
    chmod +x need-for-speed
    ./need-for-speed
    ```
    El programa mostró el mensaje `Not fast enough. BOOM!`, indicando que se había agotado el tiempo.

3. Analizamos el programa utilizando:
    ```bash
    objdump -d -M intel need-for-speed | grep -A 100 '<main>:'
    ```

4. Identificamos las funciones `set_timer`, `get_key` y `print_flag`. Para evitar el temporizador, abrimos GDB:
    ```bash
    gdb ./need-for-speed
    ```

5. Dentro de GDB ejecutamos los siguientes comandos:
    ```gdb
    break main
    run
    set $rip = main+39
    continue
    ```

6. Al saltar la función `set_timer`, el programa pudo generar la clave y mostrar la bandera:
    ```text
    academy{Good job keeping bus #30963d0f speeding along!}
    ```
## Notas adicionales
Utilizamos `objdump` para identificar las funciones del programa y GDB para modificar el flujo de ejecución. El comando `set $rip = main+39` permitió omitir el temporizador y ejecutar directamente la generación de la clave.
## Referencias