## Descripcion
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337?

## Solucion

```
nc fickle-tempest.picoctf.net 52791

NoeAH-academy@webshell:~$ nc fickle-tempest.picoctf.net 52791
Let us see how data is stored
pear
Please give the 01110000 01100101 01100001 01110010 as a word.
...
you have 45 seconds.....

Input:
pear
Please give me the  o143 o157 o154 o157 o162 o141 o144 o157 as a word.
Input:
colorado
Please give me the 6d6170 as a word.
Input:
map
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_acdCcfCa}
```

```
picoCTF{learning_about_converting_values_acdCcfCa}
```

## Notas adicionales

Abrimos tres paginas de Cyberchef: From binary, From Octal, From Hexa. Y ahi vamos poniendo las indicaciones que nos va dando la terminal.

## Referencias
https://gchq.github.io/CyberChef/#recipe=From_Binary('Space',8)&input=IDAxMTEwMDAwIDAxMTAwMTAxIDAxMTAwMDAxIDAxMTEwMDEw