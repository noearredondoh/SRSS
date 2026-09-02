## Descripción

Can you break into this super secure portal?

[http://fickle-tempest.picoctf.net:61639](http://fickle-tempest.picoctf.net:61639/)
## Solución

Al inspeccionar el código fuente de la página, se encuentra que la validación de la contraseña se realiza en el lado del cliente mediante un script de JavaScript ofuscado.

Analizando la función `verify()`, se observa que evalúa fragmentos consecutivos de la cadena usando `substring()` con saltos basados en `split = 4`

- `(0, 8)`: `picoCTF{`

- `(8, 16)`: `not_this`

- `(16, 24)`: `_again_4`

- `(24, 32)`: `daf93}`

```
picoCTF{not_this_again_4daf93}
```

## Notas adicionales

La ofuscación en cliente no brinda seguridad; las credenciales y validaciones críticas siempre deben procesarse en el servidor.

## Referencias
https://gemini.google.com/app?hl=es