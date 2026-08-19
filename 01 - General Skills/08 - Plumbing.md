## Descripcion
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?

## Solucion
```
NoeAH-academy@webshell:~$ nc fickle-tempest.picoctf.net 56819 > H

NoeAH-academy@webshell:~$ ls
H  README.txt  file  flag
NoeAH-academy@webshell:~$ cat H | grep pico
picoCTF{digital_plumb3r_d3246b6B}
NoeAH-academy@webshell:~$ 
```

```
picoCTF{digital_plumb3r_d3246b6B}
```

## Notas adicionales
Nos conectamos al servidor desde la consola y todo lo que el servidor mande de respuesta lo colocamos en una archivo en este caso H, ya solo con cat y grep buscamos la bandera

## Referencias
https://webshell.cylabacademy.org/