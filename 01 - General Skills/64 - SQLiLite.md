## Descripción

- Can you login to this website? Try to login [here](http://chatelaine.cylabacademy.net:37956/).

## Solución

```
Se accedió al formulario de login y se ingresó el payload "admin' OR '1'='1" en el campo de nombre de usuario para alterar la lógica de la consulta SQL subyacente
  
La inyección provocó que la consulta de la base de datos evaluara una condición verdaderamente constante ("WHERE username='admin' OR '1'='1'"), omitiendo la verificación de la contraseña.

Al iniciar sesión con exito, el sistema desplegó la bandera:
```

```
academy{L00k5_l1k3_y0u_solv3d_it_b57ed0cd}
```

## Notas adicionales

## Referencias

https://gemini.google.com/app?hl=es
