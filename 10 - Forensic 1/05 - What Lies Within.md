## Descripción

There's something in the [building](https://challenge-files.cylabacademy.net/library/5235bfccd8f3cc2d059ee828f774846542f28f7ec66cb4f0c6ceb536c38026d4/buildings.png). Can you retrieve the flag?

- There is data encoded somewhere... there might be an online decoder.

## Solución

```
Primero se descargo el archivo. Después, con **file buildings.png** se comprobó que era una imagen PNG. Como el reto ocultaba información mediante esteganografía, se instaló la herramienta **zsteg** con **sudo gem install zsteg**. Finalmente, se analizó la imagen con **zsteg buildings.png**, encontrando entre los datos ocultos la flag del reto.
```

```
academy{h1d1ng_1n_th3_b1t5}
```

## Notas adicionales

- zsteg es una herramienta para **detectar y extraer información escondida dentro de imágenes**, principalmente **PNG y BMP**.

## Referencias

https://gemini.google.com/app?hl=es