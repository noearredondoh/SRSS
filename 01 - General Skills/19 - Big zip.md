## Descripcion

Unzip this archive and find the flag.

- Can grep be instructed to look at every file in a directory and its subdirectories?
## Solucion

```
...
...
...
NoeAH-academy@webshell:~$ ls
Addadshashanammu      Addadshashanammu.zip.1  README.txt     big-zip-files.zip  file  ltdis.sh    ltdis.sh.2  static.1  static.2.ltdis.strings.txt  strings    warm
Addadshashanammu.zip  H                       big-zip-files  enc_flag           flag  ltdis.sh.1  static      static.2  static.2.ltdis.x86_64.txt   strings.1
NoeAH-academy@webshell:~$ grep -r "pico" big-zip-files/
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
NoeAH-academy@webshell:~$ 
```

```
picoCTF{gr3p_15_m4g1c_ef8790dc}
```

## Notas adicionales

Con `grep` usamos la herramienta de búsqueda. La opción `-r` realiza la búsqueda de forma recursiva, es decir, revisa también las subcarpetas. Después indicamos la palabra que queremos buscar y al final el directorio donde se realizará la búsqueda.

grep -r "pico" big-zip-files/
## Referencias
https://webshell.cylabacademy.org/