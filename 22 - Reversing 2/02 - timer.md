## Descripción

You will find the flag after analysing this apk Download [here](https://challenge-files.cylabacademy.net/library/b31248aec6287cbe220d0dbfa55e216b87e6175b3561d441062bfdd018f3cacc/timer.apk).

## Solución

1. Se descargó el archivo `timer.apk` y se verificó su existencia:
    ```bash
    ls -lh
    ```

2. Se descompiló la aplicación utilizando JADX:
    ```bash
    jadx -d ~/picoctf/timer/timer_decompiled ~/picoctf/timer/timer.apk
    ```

3. Se comprobaron los archivos generados:
    ```bash
    ls ~/picoctf/timer/timer_decompiled
    ```
    Se obtuvieron las carpetas `sources` y `resources`.

4. Se buscaron las cadenas que tuvieran el formato de una bandera:
    ```bash
    grep -rhoE 'academy\{[^}]+\}|picoCTF\{[^}]+\}' ~/picoctf/timer/timer_decompiled | sort -u
    ```

5. El comando encontró la bandera directamente dentro de los archivos descompilados.
```
academy{t1m3r_r3v3rs3d_succ355fully_17496}
```

## Notas adicionales

- **JADX:** Herramienta utilizada para descompilar aplicaciones Android y recuperar código Java legible.

- **APK:** Formato de archivo utilizado para distribuir e instalar aplicaciones Android.
## Referencias