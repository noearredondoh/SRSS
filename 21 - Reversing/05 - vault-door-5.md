## Descripción

In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: [VaultDoor5.java](https://challenge-files.cylabacademy.net/library/f384c32d0f8b5c3fa3ddf3f8480beefce0a3779f84f4439fb4f312f11d85c1c0/VaultDoor5.java)

## Solución

1. Se descargó el archivo `VaultDoor5.java` y se analizó su código fuente.

2. Se identificó el método `checkPassword()`, encargado de verificar la contraseña introducida.

3. Se observó que el programa primero aplicaba URL Encoding y posteriormente Base64 para codificar la contraseña.

4. Se creó un script en Python llamado `solve.py` para automatizar el proceso de decodificación.

5. Se utilizó la biblioteca `re` para extraer y unir las cadenas codificadas del código Java.

6. Se aplicó `base64.b64decode()` para recuperar el texto codificado mediante URL Encoding.

7. Posteriormente, se utilizó `unquote()` para convertir los valores hexadecimales a sus caracteres originales.

8. Finalmente, se ejecutó el script mediante `python3 solve.py`, recuperando la contraseña para formar la bandera.
```
academy{c0nv3rt1ng_fr0m_ba5e_64_92be25f1}
```

## Notas adicionales

**URL Encoding:** Es una técnica que representa determinados caracteres mediante valores hexadecimales precedidos por el símbolo `%`.
## Referencias