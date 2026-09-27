## Descripción

This website puts a two-factor prompt between you and the flag. Register an account, then take a close look at the requests your browser is actually sending. Try [here](http://chatelaine.cylabacademy.net:23308/) to find the flag
## Solución

```
Abrimos el sitio del reto y completamos el formulario de registro.

Configuramos el navegador para interceptar las peticiones utilizando **Burp Suite**.

Activamos **Intercept** y enviamos el formulario para capturar la petición HTTP.

Avanzamos hasta la petición donde se enviaba el código **OTP**.

Modificamos la petición interceptada para **eliminar el parámetro `otp`**.

Enviamos la petición modificada con **Forward**.

El servidor aceptó la solicitud sin el OTP y mostró la flag.
```

```
academy{#0TP_Bypvss_SuCc3$S_10ea7681}
```

## Notas adicionales

- Usamos burpsuite para interceptar

## Referencias

https://chatgpt.com/
