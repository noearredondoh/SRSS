## Descripción

A company stored a secret message on a server which got breached due to the admin using weakly hashed passwords. Can you gain access to the secret stored within the server?

## Solución

1. Se estableció una conexión con el servidor mediante `nc`, obteniendo un primer hash de 32 caracteres, correspondiente al algoritmo MD5.

2. Se utilizó **John the Ripper** junto con el diccionario `rockyou.txt` para descifrar el hash mediante un ataque de diccionario, obteniendo la contraseña `password123`.

3. Se introdujo la contraseña en el servidor, que proporcionó un segundo hash de 40 caracteres, correspondiente a SHA-1.

4. Se repitió el procedimiento utilizando John the Ripper con el formato `raw-sha1`, recuperando la contraseña `letmein`.

5. Posteriormente, el servidor mostró un tercer hash de 64 caracteres, correspondiente a SHA-256.

6. Se utilizó nuevamente John the Ripper con el formato `raw-sha256`, obteniendo la contraseña `qwerty098`.

7. Finalmente, se introdujo la última contraseña en el servidor, que confirmó el resultado y mostró la bandera.
```
academy{UseStr0nG_h@shEs_&PaSswDs!_a8894b1b}
```

## Notas adicionales

**John the Ripper:** Es una herramienta de auditoría de contraseñas que permite recuperar contraseñas mediante ataques de diccionario y otras técnicas.

**Rockyou.txt:** Es un diccionario que contiene millones de contraseñas conocidas, utilizado para comprobar la seguridad de contraseñas.

**Algoritmos hash:** MD5, SHA-1 y SHA-256 son funciones que transforman datos en valores de longitud fija. Aunque los hashes no se descifran directamente, las contraseñas débiles pueden recuperarse comparando sus hashes con los de palabras conocidas.

## Referencias