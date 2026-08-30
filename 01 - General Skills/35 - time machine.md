## Descripción

What was I last working on? I remember writing a note to help me remember...

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/162/challenge.zip)
## Solución

```
NoeAH-academy@webshell:~$ wget https://artifacts.picoctf.net/c_titan/162/challenge.zip
--2026-08-30 04:09:43--  https://artifacts.picoctf.net/c_titan/162/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.40, 3.160.5.18, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17739 (17K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                              100%[========================================================================================================================================>]  17.32K  --.-KB/s    in 0.005s  

2026-08-30 04:09:43 (3.74 MB/s) - 'challenge.zip' saved [17739/17739]

NoeAH-academy@webshell:~$ unzip challenge.zip
Archive:  challenge.zip
   creating: drop-in/
  inflating: drop-in/message.txt     
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/master  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/43/
 extracting: drop-in/.git/objects/43/246218ab4fc7b30e9a9dff073e012316851469  
   creating: drop-in/.git/objects/25/
 extracting: drop-in/.git/objects/25/16effb8d70e33bdd0023629b164a77225e1ec2  
   creating: drop-in/.git/objects/71/
 extracting: drop-in/.git/objects/71/2314f105348e295f8cadd7d7dc4e9fa871e9a2  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/master  
NoeAH-academy@webshell:~$ cd drop-in
NoeAH-academy@webshell:~/drop-in$ git log
NoeAH-academy@webshell:~/drop-in$ 
```

```
picoCTF{t1m3m@ch1n3_e8c98b3a}
```

## Notas adicionales

Para resolver el reto, primero se descargó el archivo desde la terminal usando el comando `wget` y se extrajo su contenido con `unzip`. Al ingresar al directorio generado (`cd drop-in`), el cual contenía un repositorio de Git, bastó con ejecutar el comando `git log` para auditar el historial de cambios. Ahí se localizó la bandera a simple vista, ya que el creador del reto la dejó escrita directamente como el mensaje de un _commit_.

## Referencias