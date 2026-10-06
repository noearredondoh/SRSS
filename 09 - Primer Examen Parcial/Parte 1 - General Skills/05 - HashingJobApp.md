## Descripción

If you want to hash with the best, beat this test! `nc chatelaine.cylabacademy.net 32729`

- You can use a commandline tool or web app to hash text
- Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

## Solución

```
1. Primero se realizó la conexión al servidor del reto utilizando Netcat con el comando:
nc chatelaine.cylabacademy.net 32729

2. Al conectarse, el servidor mostró una palabra o frase entre comillas y solicitó obtener su hash MD5. Para calcularlo se utilizó md5sum, escribiendo exactamente el texto proporcionado por el reto. Por ejemplo:

echo -n 'cockroaches' | md5sum

3. El comando devolvió el hash MD5 correspondiente, el cual se copió y se ingresó en el apartado Answer: de la conexión con Netcat. Este procedimiento se repitió con cada una de las frases proporcionadas por el servidor.

4. Después de ingresar correctamente todos los hashes solicitados, el servidor confirmó que las respuestas eran correctas y mostró la flag del reto.

```

```
academy{4ppl1c4710n_r3c31v3d_8c3fe27c}
```
## Notas adicionales

Es importante utilizar `echo -n` para evitar agregar un salto de línea al texto, ya que esto produciría un hash MD5 diferente. También se debe respetar exactamente el uso de espacios, mayúsculas y minúsculas.

## Referencias