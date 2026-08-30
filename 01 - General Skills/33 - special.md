## Descripción

Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)

## Solución

```
NoeAH-academy@webshell:~$ ssh -p 50600 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:50600 ([13.59.203.175]:50600)' can't be established.
ED25519 key fingerprint is SHA256:tJ0wuU5yBvNO/FrkHmR9iY36VJClMhKV+Hq2sxqKFmg.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:50600' (ED25519) to the list of known hosts.
ctf-player@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.17.0-1019-aws x86_64)

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

Special$ $0
I 
sh: 1: I: not found
Special$ ls
Is 
sh: 1: Is: not found
Special$ ${parameter?ls}
${parameter?ls} 
sh: 1: parameter: ls
Special$ ${:ls}
${:ls} 
sh: 1: Bad substitution
Special$ ${parameter=ls}
${parameter=ls} 
blargh
Special$ ${parameter=cat blargh}
${parameter=cat blargh} 
cat: blargh: Is a directory
Special$ ${parameter=cd blargh}
${parameter=cd blargh} 
Special$ ${parameter=ls blargh}
${parameter=ls blargh} 
flag.txt
Special$ ${parameter=cat < blargh/flag.txt}
${parameter=cat < blargh/flag.txt} 
cat: '<': No such file or directory
picoCTF{5p311ch3ck_15_7h3_w0r57_b741d1b1}Special$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
```

## Notas adicionales

- **Restricted Shell:** El entorno implementa un filtro ortográfico que bloquea la ejecución normal al cambiar las letras de los comandos a mayúsculas (ej. de `ls` a `Is`).

- **Parameter Expansion:** Se utilizó esta característica nativa de Bash (`${variable=comando}`) como método de evasión (_bypass_). Como el filtro ignora caracteres especiales (`$`, `{`, `=`, `}`), permite ejecutar comandos ocultos dentro de la estructura de la variable sin ser alterados.

- Comandos clave ejecutados:
	- `${parameter=ls}` (Para listar los directorios).
    - `${parameter=cat blargh/flag.txt}` (Para leer el contenido de la bandera evadiendo la restricción).

## Referencias