## Descripción

Do you think you can log us in? Try to see if you can login!

[http://fickle-tempest.picoctf.net:54257](http://fickle-tempest.picoctf.net:54257/)

## Solución

- Accedemos a la página web del reto e ingresamos al menú **Admin Login**.

- En el campo **Username**, ingresamos la carga útil (payload):
```
admin' OR '1'='1
```

- En el campo **Password**, ingresamos cualquier texto o lo dejamos en blanco.

- Presionamos el botón **Login**.

- Obtenemos acceso como administrador y se muestra la bandera (_flag_).

## Notas adicionales

- **Vulnerabilidad:** Inyección SQL (SQL Injection - Authentication Bypass).

- **Causa:** El servidor concatena directamente las entradas del usuario en la consulta SQL sin sanitizarlas (`SELECT * FROM users WHERE username = '$user' AND password = '$pass'`).

- **Efecto del payload:** Al inyectar `' OR '1'='1`, la condición evalúa siempre a `TRUE` (verdadero), ignorando la validación de la contraseña y permitiendo el inicio de sesión.

## Referencias