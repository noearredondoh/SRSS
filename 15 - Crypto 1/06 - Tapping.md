## Descripción

Theres tapping coming in from the wires.

## Solución

Primero, nos conectamos al servidor del reto mediante el comando `nc`, utilizando la dirección y el puerto proporcionados. Al establecer la conexión, obtuvimos un mensaje codificado en puntos y guiones, correspondiente al **código Morse**.

Posteriormente, utilizamos la herramienta de cyberchef, donde seleccionamos la operación `From Morse Code` e introdujimos el mensaje obtenido. La herramienta decodificó el contenido y nos permitió recuperar la bandera del reto.

```
ACADEMY{M0RS3C0D31SFUN88CC00F5}
```

## Notas adicionales

El código Morse es un sistema de codificación que representa letras y números mediante combinaciones de puntos y rayas. 
## Referencias

https://gchq.github.io/CyberChef/