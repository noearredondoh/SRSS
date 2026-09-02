## Descripción

Can you find the robots?

## Solución

Se navegó a la ruta raíz del archivo `robots.txt`.

El archivo contenía una directiva `Disallow` que ocultaba una página interna no indexada:
User-agent: *
Disallow: /cc6b1.html

Al acceder a dicha ruta en el navegador se visualizo la bandera

http://fickle-tempest.picoctf.net:61300/robots.txt
http://fickle-tempest.picoctf.net:61300/cc6b1.html


```
picoCTF{ca1cu1at1ng_Mach1n3s_cc6b1}
```

## Notas adicionales

El comando curl le pasas un sitio web y te muestra la consola

## Referencias

https://chatgpt.com/
