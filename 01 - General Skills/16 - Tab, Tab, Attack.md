## Descripcion

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames.
## Solucion

```
Solución 1
NoeAH-academy@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/1d211441eced2214a10b0c2aacbf05d153aafcd6edc055f913cafcdb48a0b02b/Addadshashanammu.zip
--2026-08-25 02:32:15--  https://challenge-files.picoctf.net/c_wily_courier/1d211441eced2214a10b0c2aacbf05d153aafcd6edc055f913cafcdb48a0b02b/Addadshashanammu.zip
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.64, 3.160.5.95, 3.160.5.40, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 5166 (5.0K) [application/octet-stream]
Saving to: 'Addadshashanammu.zip.1'

Addadshashanammu.zip.1                                     100%[========================================================================================================================================>]   5.04K  --.-KB/s    in 0s      

2026-08-25 02:32:15 (576 MB/s) - 'Addadshashanammu.zip.1' saved [5166/5166]

NoeAH-academy@webshell:~$ ls
Addadshashanammu.zip  Addadshashanammu.zip.1  H  README.txt  file  flag  ltdis.sh  ltdis.sh.1  ltdis.sh.2  static  static.1  static.2  static.2.ltdis.strings.txt  static.2.ltdis.x86_64.txt  strings  strings.1  warm
NoeAH-academy@webshell:~$ 
NoeAH-academy@webshell:~$ 
NoeAH-academy@webshell:~$ 
NoeAH-academy@webshell:~$ 
NoeAH-academy@webshell:~$ 
NoeAH-academy@webshell:~$ 
NoeAH-academy@webshell:~$ 
NoeAH-academy@webshell:~$ 
NoeAH-academy@webshell:~$ cd Addadshashanammu.zip.1
-bash: cd: Addadshashanammu.zip.1: Not a directory
NoeAH-academy@webshell:~$ cd
NoeAH-academy@webshell:~$ 
NoeAH-academy@webshell:~$ cd Addadshashanammu.zip. /
-bash: cd: too many arguments
NoeAH-academy@webshell:~$ strings Addadshashanammu.zip.1 | grep pico
printf("*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}\n");
NoeAH-academy@webshell:~$ 

```

```
Solución 2
NoeAH-academy@webshell:~$ unzip Addadshashanammu.zip.1
Archive:  Addadshashanammu.zip.1
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
 extracting: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet.c  
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
NoeAH-academy@webshell:~$ cd A
-bash: cd: A: No such file or directory
NoeAH-academy@webshell:~$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
NoeAH-academy@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet  fang-of-haynekhtnamet.c
NoeAH-academy@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./ fang-of-haynekhtnamet
-bash: ./: Is a directory
NoeAH-academy@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
NoeAH-academy@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ 
```

## Notas adicionales

^a -  va al inicio de la linea de comando
^e - va al final de la linea del comando

Hay dos soluciones:
- En la primera hacemos uso de strings y buscamos directamente la bandera
- En la segunda descomprimimos el archivo y al ingresar con ayuda de tab nos dirigimos hasta el fondo de el directorio llegando a un archivo el cual solo ejecutamos y obtenemos la bandera

## Referencias
https://webshell.cylabacademy.org/