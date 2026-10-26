## Descripción

This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://challenge-files.cylabacademy.net/library/6f9f73cad1f487b96f883f6461ef83ce482da6468064c7ed3833cd67e0525385/VaultDoor4.java)
## Solución

1. Se descargó el archivo `VaultDoor4.java` y se analizó su código fuente.

2. Se identificó el método `checkPassword()`, que contenía un arreglo llamado `myBytes` con 32 valores.

3. Se observó que los valores estaban representados en diferentes formatos: decimal, hexadecimal, octal y caracteres.

4. Se creó un script en Python llamado `solve.py` para extraer automáticamente los valores del arreglo.

5. Se utilizó la función `int()` para convertir los números según su base y `chr()` para transformarlos en caracteres ASCII.

6. Se corrigieron errores relacionados con elementos vacíos e indentación durante la ejecución del script.

7. Finalmente, se ejecutó `python3 solve.py`, reconstruyendo la contraseña original para formar la bandera.
```
academy{jU5t_4_bUnCh_0f_bYt3s_86c843fd10}
```

## Notas adicionales


## Referencias