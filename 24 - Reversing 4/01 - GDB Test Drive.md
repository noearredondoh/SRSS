## Descripción

Can you get the flag? Download this [binary](https://challenge-files.cylabacademy.net/library/394cd9dfa2b4d40f74f2ad999c1ea208ed4daf3382f56b3372ca33b69756a65d/gdbme).

Here's the test drive instructions:

- `$ chmod +x gdbme`
- `$ gdb gdbme`
- `(gdb) layout asm`
- `(gdb) break *(main+99)`
- `(gdb) run`
- `(gdb) jump *(main+104)`

## Solución

1. Descargamos el archivo `gdbme` desde la página del reto.

2. Le otorgamos permisos de ejecución:
    ```bash
    chmod +x gdbme
    ```

3. Instalamos GDB y abrimos el archivo:
    ```bash
    sudo apt update
    sudo apt install gdb
    gdb gdbme
    ```

4. Dentro de GDB ejecutamos los siguientes comandos:
    ```gdb
    set disassembly-flavor intel
    layout asm
    break *(main+99)
    run
    jump *(main+104)
    ```

5. El comando `break` colocó un punto de interrupción y `jump` permitió saltar a otra instrucción del programa, evitando la parte que impedía mostrar la bandera.

6. Finalmente, el programa mostró la bandera:
    ```text
    academy{d3bugg3r_dr1v3_ff5329f1}
    ```
## Notas adicionales
GDB es un depurador que permite analizar y controlar la ejecución de programas. En este reto lo utilizamos para modificar el flujo de ejecución y obtener la bandera.
## Referencias