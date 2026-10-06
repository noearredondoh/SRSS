## Descripción

Decode this [message](https://challenge-files.cylabacademy.net/library/d825fde6581b1311eafdd403da1cc96f1f98fe3fe84cd71d850310ebb3908088/message.wav) from the moon.

- How did pictures from the moon landing get sent back to Earth?
- What is the CMU mascot?, that might help select a RX option

## Solución

```
Buscamos sstv y luego buscamos el sstv decoder git y entonces entramos al primer 
link.
Despues clonamos, nos movemos a la carpeta e instalamos la herramienta
te regresas a donde esta el wav y ahi corremos sstv -d message.wav -o flag.png
Abrimos la imagen creada la rotamos o por defecto le pedimos ayuda a una IA para que nos de el texto de la imagen
```

```
picoCTF{beep_boop_im_in_space}
```

## Notas adicionales

## Referencias