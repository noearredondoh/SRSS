## Descripción

This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://challenge-files.cylabacademy.net/library/60e8fbcf22f4bfa0e9856c1ebbd5506050d5f0ab9fb013f9e3e175021205869b/VaultDoor1.java)

## Solución

1. Se descargó el archivo `VaultDoor1.java`, que contenía el código fuente del programa.

2. Se analizó el método `checkPassword()`, identificando que la contraseña estaba formada por 32 caracteres.

3. Se observaron múltiples condiciones con `password.charAt()`, que indicaban el carácter correspondiente a cada posición.

4. Se creó un script en Python llamado `solve.py` para reconstruir automáticamente la contraseña.

5. Se utilizó la biblioteca `re` para identificar las posiciones y los caracteres mediante expresiones regulares.

6. Se ordenaron los caracteres en sus posiciones correspondientes y se reconstruyó la contraseña original.

7. Finalmente, se ejecutó el script mediante `python3 solve.py`, obteniendo la bandera del reto.
```
academy{d35cr4mbl3_tH3_cH4r4cT3r5_45ebc3}
```

## Notas adicionales

**Ingeniería inversa:** Es una técnica que permite analizar el funcionamiento de un programa para comprender su lógica y recuperar información.
## Referencias