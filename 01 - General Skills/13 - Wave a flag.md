## Descripcion
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...

- This program will only work in the webshell or another Linux computer.
- To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget where the url can be found in the details section.
- Run this program by entering the following in the Terminal prompt: $ ./warm, but you'll first have to make it executable with $ chmod +x warm
- -h and --help are the most common arguments to give to programs to get more information from them!
- Not every program implements help features like -h and --help.

## Solucion

```
NoeAH-academy@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/70013ed41d4cfe2bb48628471dac6fc12238b5dbe164301ae3b4e35277b1e80b/warm
--2026-08-25 02:17:07--  https://challenge-files.picoctf.net/c_wily_courier/70013ed41d4cfe2bb48628471dac6fc12238b5dbe164301ae3b4e35277b1e80b/warm
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.95, 3.160.5.64, 3.160.5.18, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19312 (19K) [application/octet-stream]
Saving to: 'warm'

warm                                                       100%[========================================================================================================================================>]  18.86K  --.-KB/s    in 0.008s  

2026-08-25 02:17:07 (2.41 MB/s) - 'warm' saved [19312/19312]

NoeAH-academy@webshell:~$ file warm
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=9e46ec8729d2f2aa8ffc4b1cdc058081bddcfe67, for GNU/Linux 3.2.0, with debug_info, not stripped
NoeAH-academy@webshell:~$ chmod +x warm
NoeAH-academy@webshell:~$ . /warm 
-bash: /warm: No such file or directory
NoeAH-academy@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
NoeAH-academy@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
NoeAH-academy@webshell:~$ 
```

```
 picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
```

## Notas adicionales
Descargamos el archivo y verificamos que tipo de archivo es, como es un ejecutable le damos permisos de ejecucion con chmod y al ejecutarlo este manda un mensaje que necesita -h para lectura y al agregarlo manda la bandera.

./warm -ejecuta el binario una vez ue ya tiene los permisos de ejecucuon ElF es el formato de archivo ejecutable en liniux como el .exe de windows

file warm: ver que tipo de archivo es.

## Referencias
https://webshell.cylabacademy.org/