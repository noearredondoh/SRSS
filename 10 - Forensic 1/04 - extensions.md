## Descripción

This is a really weird text file. Can you find the flag? Get the flag from [TXT](https://challenge-files.cylabacademy.net/library/a5d365fedad883763fb28c78e25a1765220bef6501848c84f2a7a7adf74d83cd/flag.txt)

1. How do operating systems know what kind of file it is? (It's not just the ending!)
2. Make sure to submit the flag as academy{XXXXX}
## Solución

```
Primero se descargo el archivo y se utilizó ls para localizar el archivo flag.txt. Después, con file flag.txt se identificó que el archivo realmente era una imagen PNG y no un archivo de texto. Se cambió su extensión con **mv flag.txt flag.png** y finalmente se abrió usando **xdg-open flag.png**, mostrando la imagen que contenía la flag.
```

```
academy{now_you_know_about_extensions}
```
## Notas adicionales

## Referencias