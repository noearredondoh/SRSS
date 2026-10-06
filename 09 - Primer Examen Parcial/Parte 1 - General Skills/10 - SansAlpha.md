## Descripción

The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols. `ssh -p 23158 ctf-player@xebec.cylabacademy.net`

Use password: `fa1a82ad`

HINTS 1 Where can you get some letters?

## Solución

```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ ssh -p 41484 ctf-player@xebec.cylabacademy.net
The authenticity of host '[xebec.cylabacademy.net]:41484 ([3.14.181.178]:41484)' can't be established.
ED25519 key fingerprint is: SHA256:nalfXhowfu1stSyT0M4F6ZC1kzwfaCJibpzyUyiqt/U
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:1: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[xebec.cylabacademy.net]:41484' (ED25519) to the list of known hosts.
ctf-player@xebec.cylabacademy.net's password:
Welcome to Ubuntu 24.04.4 LTS (GNU/Linux 7.0.0-1013-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

SansAlpha$ /*/????64 */*
\x1b[?2004h\x1b[?2004l
/bin/base64: extra operand ‘blargh/flag.txt’
Try '/bin/base64 --help' for more information.
\x1b[?2004h
SansAlpha$ /???/????32 */*
\x1b[?2004l
/bin/base32: extra operand ‘blargh/on-alpha-9.txt’
Try '/bin/base32 --help' for more information.
\x1b[?2004h
SansAlpha$ /???/????32 */????.???
\x1b[?2004l
OJSXI5LSNYQDAIDBMNQWIZLNPF5TO2BRGVPW25JRG4YXMM3SGUZV6MJVL5WTIZDOGM2TKX3CMQ2D
SZLFGNTH2===
\x1b[?2004h


from base 32
academy{7h15_mu171v3r53_15_m4dn355_bd49ee3f}

```

## Notas adicionales

./* es una forma para que vea el sistema algun archivo o algo

## Referencias

https://medium.com/@0xVirtu4l/picoctf-2024-sansalpha-challenge-solve-c754ee1deba4