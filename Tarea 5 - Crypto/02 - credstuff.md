## Descripción

We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it? Download the leak [here](https://challenge-files.cylabacademy.net/library/7f760cee144ac7237469fd6bfab7c748d6f1d101ca47c101187ca7d8f5c721f0/leak.tar).

The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.

## Solución

1. Se descargó el archivo `leak.tar` y se descomprimió mediante el comando `tar -xvf leak.tar`.

2. Se obtuvieron dos archivos: `usernames.txt`, que contenía los nombres de usuario, y `passwords.txt`, con sus respectivas contraseñas.

3. Se utilizó el comando `grep -ni 'cultiris' leak/usernames.txt` para localizar al usuario, encontrándolo en la línea 378.

4. Mediante el comando `sed -n '378p' leak/passwords.txt`, se obtuvo la contraseña correspondiente.

5. Se observó que la contraseña tenía una estructura similar a una bandera, por lo que se identificó la posibilidad de que estuviera cifrada con ROT13.

6. Se aplicó el descifrado mediante el comando `tr 'A-Za-z' 'N-ZA-Mn-za-m'`, obteniendo la bandera original.
```
academy{C7r1F_54V35_71M3}
```

## Notas adicionales

**ROT13:** Es una variante del cifrado César que sustituye cada letra por otra situada 13 posiciones adelante en el alfabeto. Al aplicarlo dos veces, se recupera el texto original.

## Referencias