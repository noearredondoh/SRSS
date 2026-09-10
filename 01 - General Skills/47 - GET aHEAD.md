## Descripción

Find the flag being held on this server to get ahead of the competition

http://wily-courier.picoctf.net:55583/

## Solución

Para resolver el reto se realizó una petición HTTP utilizando el método `HEAD` (sugerido por el nombre del reto "aHEAD") para inspeccionar únicamente los encabezados (_headers_) de la respuesta del servidor, evitando descargar el cuerpo del mensaje. Se ejecutó el siguiente comando en la consola de desarrollador del navegador:

```
fetch('http://wily-courier.picoctf.net:55583/', { method: 'HEAD' })
  .then(res => console.log([...res.headers]))
```

## Notas adicionales

- **Método HEAD:** A diferencia de `GET` o `POST`, el método HTTP `HEAD` solicita que el servidor responda únicamente con los encabezados HTTP sin transferir el cuerpo del documento HTML
- Se puede resolver alternativamente mediante la terminal usando el comando `curl -I <URL>`

## Referencias