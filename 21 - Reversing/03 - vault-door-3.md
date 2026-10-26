## Descripción

This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://challenge-files.cylabacademy.net/library/64ed47ea66574a28e2f23bbe36be348987a9ff131641bf451b1c04bb7b3e2d9f/VaultDoor3.java)

## Solución

1. Se descargó el archivo `VaultDoor3.java`, que contenía el código fuente del programa.

2. Se analizó el método `checkPassword()`, identificando que la contraseña debía contener 32 caracteres.

3. Se encontraron cuatro ciclos `for` que modificaban las posiciones de los caracteres dentro de un arreglo llamado `buffer`.

4. Se identificó la cadena utilizada en el método `equals()`, con la que se comparaba la contraseña transformada.

5. Se creó un script en Python llamado `solve.py` para invertir las operaciones realizadas por los ciclos.

6. Se reconstruyó la contraseña original colocando cada carácter en su posición correspondiente.

7. Finalmente, se ejecutó el script mediante `python3 solve.py`, obteniendo la contraseña para formar la bandera.
```
academy{jU5t_a_s1mpl3_an4gr4m_4_u_e7de62}
```

## Notas adicionales

**Ingeniería inversa:** Es una técnica que permite analizar el funcionamiento de un programa para comprender su lógica y recuperar información.

## Referencias