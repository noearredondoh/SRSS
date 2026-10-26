## Descripción

Your mission is to enter Dr. Evil's laboratory and retrieve the blueprints for his Doomsday Project. The laboratory is protected by a series of locked vault doors. Each door is controlled by a computer and requires a password to open. Unfortunately, our undercover agents have not been able to obtain the secret passwords for the vault doors, but one of our junior agents obtained the source code for each vault's computer! You will need to read the source code for each level to figure out what the password is for that vault door. As a warmup, we have created a replica vault in our training facility.

The source code for the training vault is here: [VaultDoorTraining.java](https://challenge-files.cylabacademy.net/library/080a285021cd4d6edaff96f54c7eba477b4f450b778c0c129297bf51bbd3d3c8/VaultDoorTraining.java)

## Solución

1. Se descargó el archivo `VaultDoorTraining.java`, que contenía el código fuente del programa.

2. Se visualizó su contenido mediante el comando `cat VaultDoorTraining.java`.

3. Se analizó el código y se identificó el método `checkPassword()`, encargado de verificar la contraseña introducida.

4. Dentro del método se encontró la función `password.equals()`, que comparaba la contraseña del usuario con una cadena escrita directamente en el código.

5. Se extrajo la contraseña y se colocó dentro del formato `academy{...}` para obtener la bandera.

```
academy{w4rm1ng_Up_w1tH_jAv4_1633b42d7f1}
```

## Notas adicionales

**Ingeniería inversa:** Es una técnica que permite analizar el funcionamiento de un programa para comprender su lógica e identificar información importante.

## Referencias
https://github.com/hackadvisermx/cylab-picoctf