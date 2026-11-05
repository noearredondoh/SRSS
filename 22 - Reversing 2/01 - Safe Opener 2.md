## Descripción

What can you do with this file? I forgot the key to my safe but this [file](https://challenge-files.cylabacademy.net/library/5c5f8143dd09275a5ecdd390027ea5488159881d757099706515c4cbf15992f1/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?
## Solución

1. Se descargó el archivo `SafeOpener.class` y se comprobó su existencia:
    ```bash
    ls -lh
    ```

2. Se intentó analizar el código compilado utilizando `javap`:
    ```bash
    javap -c -p SafeOpener.class
    ```
    Sin embargo, la herramienta no estaba instalada.

3. Se examinó directamente el contenido del archivo:
    ```bash
    cat SafeOpener.class
    ```
    Entre los datos binarios se identificó una cadena que contenía la bandera.

4. Para localizar la bandera de manera más sencilla, se puede utilizar:
    ```bash
    strings SafeOpener.class | grep 'academy{'
    ```
    Este comando busca las cadenas de texto legibles que contienen el formato de la bandera.
```
academy{SAf3_0p3n3rr_y0u_solv3d_it_7f70e636}
```
## Notas adicionales

## Referencias