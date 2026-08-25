## Descripcion
Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/a35dc624cfda858ed12a4bce57f832dad3b433bad6cde2b98e25fae4bc8ff760/strings) without running it?

## Solucion

```
NoeAH-academy@webshell:~$ wget https://challenge-files.picoctf.net/c_fickle_tempest/563d66bbed3925c75ed71efa974bfafab26460ae99938d699a8881cd173fca60/strings
--2026-08-25 02:02:40--  https://challenge-files.picoctf.net/c_fickle_tempest/563d66bbed3925c75ed71efa974bfafab26460ae99938d699a8881cd173fca60/strings
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.40, 3.160.5.95, 3.160.5.64, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 784424 (766K) [application/octet-stream]
Saving to: 'strings.1'

strings.1                                                  100%[========================================================================================================================================>] 766.04K  1.86MB/s    in 0.4s    

2026-08-25 02:02:41 (1.86 MB/s) - 'strings.1' saved [784424/784424]

NoeAH-academy@webshell:~$ ls -la
total 1904
drwxr-xr-x 3 NoeAH-academy NoeAH-academy   4096 Aug 25 02:02 .
drwxr-xr-x 3 root          root              55 Aug 17 16:47 ..
-rw------- 1 NoeAH-academy NoeAH-academy   1169 Aug 24 17:16 .bash_history
-rw-r--r-- 1 NoeAH-academy NoeAH-academy    220 Aug 17 16:47 .bash_logout
-rw-r--r-- 1 NoeAH-academy NoeAH-academy   3771 Aug 17 16:47 .bashrc
-rw-r--r-- 1 NoeAH-academy NoeAH-academy    807 Aug 17 16:47 .profile
-rw------- 1 NoeAH-academy NoeAH-academy     55 Aug 19 16:48 .python_history
drwx------ 2 NoeAH-academy NoeAH-academy     48 Aug 24 17:11 .ssh
-rw-rw-r-- 1 NoeAH-academy NoeAH-academy   5166 Dec 12  2025 Addadshashanammu.zip
-rw-rw-r-- 1 NoeAH-academy NoeAH-academy 288001 Aug 19 19:49 H
-rw-r--r-- 1 root          root            4510 Aug 25 01:51 README.txt
-rw-rw-r-- 1 NoeAH-academy NoeAH-academy  14546 Oct 31  2025 file
-rw-rw-r-- 1 NoeAH-academy NoeAH-academy     34 Dec 12  2025 flag
-rwxrwxr-x 1 NoeAH-academy NoeAH-academy    785 Dec 12  2025 ltdis.sh
-rw-rw-r-- 1 NoeAH-academy NoeAH-academy  16776 Dec 12  2025 static
-rw-rw-r-- 1 NoeAH-academy NoeAH-academy 784424 Nov 14  2025 strings
-rw-rw-r-- 1 NoeAH-academy NoeAH-academy 784424 Nov 14  2025 strings.1
NoeAH-academy@webshell:~$ chmod +x strings
NoeAH-academy@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_dB2CEA76}
```

```
picoCTF{5tRIng5_1T_dB2CEA76}
```

## Notas adicionales

- Descargar el archivo en la consola con `wget`.
- Verificar que se haya descargado con `ls`.
- Usar `strings` para extraer el texto legible del archivo.
- Usar `grep` para filtrar y buscar directamente la flag.

## Referencias
https://webshell.cylabacademy.org/