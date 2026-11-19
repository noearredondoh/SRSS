## Descripción

We have recovered a [binary](https://challenge-files.cylabacademy.net/library/3c06dee37ca661aa44d0cdd3193b89065bbed43cadb4663740d63c64b9d238c0/rev) and a [text file](https://challenge-files.cylabacademy.net/library/3c06dee37ca661aa44d0cdd3193b89065bbed43cadb4663740d63c64b9d238c0/rev_this). Can you reverse the flag.

1. objdump and Gihdra are some tools that could assist with this

## Solución

1. Descargamos los archivos `rev` y `rev_this` desde la página del reto.

2. Analizamos el código ensamblador del programa utilizando:
    ```bash
    objdump -d -M intel rev | grep -A 100 '<main>:'
    ```

3. Identificamos que el programa cifraba los caracteres de las posiciones 8 a 22, sumando `5` en posiciones pares y restando `2` en posiciones impares.

4. Creamos un script en Python para invertir el cifrado:
    ```bash
    nano solve.py
    ```
    Introdujimos el siguiente código:
    ```python
    with open("rev_this", "rb") as f:
        data = bytearray(f.read())
    
    for i in range(8, 23):
        if i % 2 == 0:
            data[i] = (data[i] - 5) % 256
        else:
            data[i] = (data[i] + 2) % 256
    
    print(data.decode())
    ```

4. Guardamos el archivo y ejecutamos:
    ```bash
    python3 solve.py
    ```

5. El programa descifró el contenido de `rev_this` y obtuvimos la bandera:
    ```text
    academy{r3v3rs354680934}
    ```
## Notas adicionales
Utilizamos `objdump` para identificar las operaciones del programa original y Python para invertirlas. El cifrado modificaba los valores ASCII de los caracteres dependiendo de su posición.
## Referencias