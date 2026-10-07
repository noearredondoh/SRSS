## Descripción

🥛 [http://xebec.cylabacademy.net:20578/](http://xebec.cylabacademy.net:20578/)


## Solución

Abrimos el link que nos da el reto, despues copiamos la imagen que nos aparece. Posteriormente, se descargó desde la terminal mediante `wget` y se verificó con el comando `file`, observando que se trataba de una imagen PNG de **1280 × 47520 píxeles**.

Se utilizó la herramienta `zsteg` para analizar los bits de la imagen en busca de información oculta. Debido a las grandes dimensiones del archivo, inicialmente `zsteg` produjo el error `stack level too deep`, por lo que se aumentó el tamaño de la pila de Ruby mediante:
```
export RUBY_THREAD_VM_STACK_SIZE=500000000
```

Despues se volvio a ejecutar:
```
zsteg concat_v.png
```

El análisis permitió localizar la información escondida mediante **esteganografía LSB (Least Significant Bit)** y obtener finalmente la bandera del reto.
```
academy{imag3_m4n1pul4t10n_sl4p5}
```

## Notas adicionales

La imagen tenía una altura inusualmente grande, lo que provocaba errores durante su análisis. Fue necesario aumentar el tamaño de la pila de Ruby para que `zsteg` pudiera procesarla correctamente

## Referencias