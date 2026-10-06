## Descripción

Python scripts are invoked kind of like programs in the Terminal... Can you run [ende.py](https://challenge-files.cylabacademy.net/library/6d20533ced9029ce644ff2c2bcaaa8a7c95b46963bfde810a8d69484d1db4ccd/ende.py) using [password.txt](https://challenge-files.cylabacademy.net/library/6d20533ced9029ce644ff2c2bcaaa8a7c95b46963bfde810a8d69484d1db4ccd/password.txt) to get [flag.txt.en](https://challenge-files.cylabacademy.net/library/6d20533ced9029ce644ff2c2bcaaa8a7c95b46963bfde810a8d69484d1db4ccd/flag.txt.en)?

- Get the Python script accessible in your shell by entering the following command in the Terminal prompt: `$ wget` followed by a link to the script. The link can be copied from the details section.
- `$ man python`

## Solución

```
Primero se descargaron los archivos necesarios para realizar el reto: ende.py, password.txt y flag.txt.en. Después se verificó que estuvieran disponibles en la terminal.

Para conocer la contraseña necesaria para descifrar el archivo se utilizó:
cat password.txt

Después se ejecutó el programa de Python en modo de descifrado sobre el archivo que contenía la flag cifrada:
python3 ende.py -d flag.txt.en

El programa solicitó una contraseña. Se copió la obtenida anteriormente de password.txt y se ingresó en la terminal. Al ser correcta, el programa descifró el contenido y mostró la flag del reto.
```

```
academy{4p0110_1n_7h3_h0us3_d6af8f37}
```

## Notas adicionales

## Referencias