## Descripción

The flag is somewhere on this web application not necessarily on the website. Find it. Check [this](http://xebec.cylabacademy.net:24258/) out.
## Solución

```
Se accedió a "/robots.txt" en la URL del reto y se encontró una cadena codificada en la lista.

Se convirtió la cadena de **Base64 a texto plano** para obtener la ruta oculta en el servidor.

Se navegó a la ruta decodificada desde el navegador para desplegar la bandera:
```

```
academy{Who_D03sN7_L1k5_90B0T5_662b27d3}
```

## Notas adicionales

## Referencias

https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)