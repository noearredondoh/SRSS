## Descripcion

Unzip this archive and find the file named 'uber-secret.txt'
## Solucion

```
NoeAH-academy@webshell:~$ wget https://artifacts.picoctf.net/c/501/files.zip
--2026-08-25 03:13:54--  https://artifacts.picoctf.net/c/501/files.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.40, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3995553 (3.8M) [application/octet-stream]
Saving to: 'files.zip'

files.zip                                                  100%[========================================================================================================================================>]   3.81M  1.83MB/s    in 2.1s    

2026-08-25 03:13:56 (1.83 MB/s) - 'files.zip' saved [3995553/3995553]

NoeAH-academy@webshell:~$ ls
Addadshashanammu      Addadshashanammu.zip.1  README.txt     big-zip-files.zip  file       flag      ltdis.sh.1  static    static.2                    static.2.ltdis.x86_64.txt  strings.1
Addadshashanammu.zip  H                       big-zip-files  enc_flag           files.zip  ltdis.sh  ltdis.sh.2  static.1  static.2.ltdis.strings.txt  strings                    warm
NoeAH-academy@webshell:~$ unzip files.zip
Archive:  files.zip
   creating: files/
   creating: files/satisfactory_books/
   creating: files/satisfactory_books/more_books/
  inflating: files/satisfactory_books/more_books/37121.txt.utf-8  
  inflating: files/satisfactory_books/23765.txt.utf-8  
  inflating: files/satisfactory_books/16021.txt.utf-8  
  inflating: files/13771.txt.utf-8   
   creating: files/adequate_books/
   creating: files/adequate_books/more_books/
   creating: files/adequate_books/more_books/.secret/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt  
  inflating: files/adequate_books/more_books/1023.txt.utf-8  
  inflating: files/adequate_books/46804-0.txt  
  inflating: files/adequate_books/44578.txt.utf-8  
   creating: files/acceptable_books/
   creating: files/acceptable_books/more_books/
  inflating: files/acceptable_books/more_books/40723.txt.utf-8  
  inflating: files/acceptable_books/17880.txt.utf-8  
  inflating: files/acceptable_books/17879.txt.utf-8  
  inflating: files/14789.txt.utf-8   
NoeAH-academy@webshell:~$ find . -name "uber-secret.txt"
./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
NoeAH-academy@webshell:~$ cat ./files/something/uber-secret.txt
cat: ./files/something/uber-secret.txt: No such file or directory
NoeAH-academy@webshell:~$ cat ./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
picoCTF{f1nd_15_f457_ab443fd1}
NoeAH-academy@webshell:~$ 
```

```
picoCTF{f1nd_15_f457_ab443fd1}
```

## Notas adicionales

Primero se descomprimió el archivo ZIP con `unzip`. Después se utilizó el comando `find` junto con `-name` para localizar el archivo `uber-secret.txt` dentro de todas las subcarpetas. Una vez encontrada la ruta exacta, se utilizó `cat` para leer su contenido y obtener la flag.

```
unzip files.zip
find . -name "uber-secret.txt"
cat ruta_del_archivo
```

`find` busca archivos o directorios, `-name` permite indicar el nombre exacto que queremos localizar y `cat` muestra el contenido del archivo.


## Referencias
https://webshell.cylabacademy.org/