## Descripción

Can you break into this super secure portal?

[http://fickle-tempest.picoctf.net:62922](http://fickle-tempest.picoctf.net:62922/)

Never trust the client
## Solución

Se inspeccionó el código fuente HTML del sitio, donde se localizó una función JavaScript encargada de verificar la contraseña en el lado del cliente.

```
picoCTF{no_clients_plz_2eb02b45}
```

## Notas adicionales

La lógica de autenticación nunca debe residir en el cliente, ya que el código en el navegador es completamente visible y modificable por el usuario.
## Referencias
https://chatgpt.com/