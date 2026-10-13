## Descripción

We made a lot of substitutions to encrypt this. Can you decrypt it?

## Solución

Primero, nos conectamos al servidor del reto mediante el comando `nc`, obteniendo un mensaje cifrado mediante **sustitución monoalfabética**.

Posteriormente, utilizamos la herramienta quipqiup, donde introdujimos el mensaje cifrado completo. Al presionar `Solve`, la herramienta realizó un análisis de frecuencia y logró descifrar el texto.

En el primer resultado apareció la frase _"congrats here is your flag"_, seguida de la bandera, la cual introdujimos directamente en CyLab Academy sin utilizar el formato `academy{}`.

```
frequency_is_c_over_lambda_vddcgoslot
```

## Notas adicionales

El cifrado por sustitución monoalfabética consiste en reemplazar cada letra del mensaje original por otra letra del alfabeto. Herramientas como quipqiup permiten descifrar estos mensajes mediante análisis de frecuencia y patrones del idioma.

## Referencias

https://quipqiup.com/