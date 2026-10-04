## Descripción

Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...

- This program will only work in the webshell or another Linux computer.
- To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget where the url can be found in the details section.
- Run this program by entering the following in the Terminal prompt: $ ./warm, but you'll first have to make it executable with $ chmod +x warm
- -h and --help are the most common arguments to give to programs to get more information from them!
- Not every program implements help features like -h and --help.


## Solución

```
1. Descargar el archivo binario del reto usando wget

2. Inspeccionar el tipo de archivo para verificar que sea un ejecutable de Linux
file warm
Salida: warm: ELF 64-bit LSB pie executable, x86-64...

3. Otorgar permisos de ejecución al archivo binario
chmod +x warm

4. Ejecutar el programa en el directorio actual para ver su comportamiento
./warm
Salida: Hello user! Pass me a -h to learn what I can do!

5. Ejecutar el programa pasando el argumento de ayuda (-h) para obtener la flag
./warm -h
```

```
picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
```


## Notas adicionales

- Descargamos el archivo y verificamos que tipo de archivo es, como es un ejecutable le damos permisos de ejecucion con chmod y al ejecutarlo este manda un mensaje que necesita -h para lectura y al agregarlo manda la bandera.

- ./warm -ejecuta el binario una vez ue ya tiene los permisos de ejecucuon ElF es el formato de archivo ejecutable en liniux como el .exe de windows

- file warm: ver que tipo de archivo es.

## Referencias