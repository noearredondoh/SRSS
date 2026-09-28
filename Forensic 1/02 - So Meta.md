## Descripción

Find the flag in this [picture](https://challenge-files.cylabacademy.net/library/c0f3e512631112c251ffec94d2ffd27689fccdde3f8ee08fae4b0c05b25aa818/pico_img.png)

1. What does meta mean in the context of files?
2. Ever heard of metadata?
## Solución

```
**Decarga el archivo**
wget https://challenge-files.cylabacademy.net/library/e78198c6a7dc5e471e8429d4953e7595feafe17764258eec169b8dab8bb3c925/garden.jpg](https://challenge-files.cylabacademy.net/library/c0f3e512631112c251ffec94d2ffd27689fccdde3f8ee08fae4b0c05b25aa818/pico_img.png

**Extracción de la bandera**
strings pico_img.png | grep academy
```

```
academy{s0_m3ta_b9d1ec99}
```

## Notas adicionales

Al ejecutar `strings`, analizó los datos binarios de la imagen y filtró las cadenas legibles de texto con 10 o más caracteres. Esto permitió encontrar la _flag_ oculta al final del archivo sin distorsionar el visor.

## Referencias