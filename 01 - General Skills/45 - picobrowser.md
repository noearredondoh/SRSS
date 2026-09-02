## Descripción

This website can be rendered only by picobrowser, go and catch the flag!

[http://fickle-tempest.picoctf.net:63260](http://fickle-tempest.picoctf.net:63260/)

## Solución

Se abrieron las **Herramientas de Desarrollador** en el navegador. Despues desde el menú de comandos se accedió al panel **Network conditions**.

Se desmarcó la opción **Use browser default** en la sección _User agent_ y se ingresó manualmente el valor `picobrowser`

Al recargar la página y solicitar la bandera, el servidor validó la cabecera manipulada y entregó la flag:

```
picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}
```

## Notas adicionales

Alternativa por consola: también puede resolverse directamente ejecutando

```
curl -H "User-Agent: picobrowser" [http://fickle-tempest.picoctf.net:63260/flag](http://fickle-tempest.picoctf.net:63260/flag)
```


## Referencias

https://gemini.google.com/app?hl=es