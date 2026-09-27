## Descripción

Can you get the flag? Go to this [website](http://xebec.cylabacademy.net:36823/) and see what you can discover.

## Solución

```
Se abrió el sitio web y se inspeccionó el código fuente de la página (`Ctrl + U`) tras intentar un inicio de sesión fallido.
  
En los archivos de JavaScript cargados (específicamente en `secure.js`), se identificaron las credenciales de acceso codificadas en texto plano:

- **Usuario:** `admin`
- **Contraseña:** `strongPassword098765`
   
Al ingresar estas credenciales en el formulario de inicio de sesión, el sitio validó el acceso y desplegó la bandera
```

```
academy{j5_15_7r4n5p4r3n7_df9583b6}
```

## Notas adicionales

- El desarrollador cometió el error crítico de delegar la validación de acceso al navegador del usuario (_client-side_) en lugar de procesarla de forma segura en el servidor (_backend_), exponiendo datos sensibles en el código fuente frontend.
## Referencias