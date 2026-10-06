## Descripción

Help us test the form by submiting the username as `test` and password as `test!`  The website running [here](http://xebec.cylabacademy.net:31448/)

## Solución

```
1. Enviar el formulario de autenticación mediante POST con las credenciales asignadas
Credenciales: username=test password=test!

2. Interceptar la secuencia de redirecciones HTTP 302 (Found) utilizando DevTools (Keep log) o cURL
Primera redirección interceptada en la cabecera Location:
/next-page/id=YWNhZGVteTwtcm94aWVzX2Fs

Segunda redirección interceptada en la cabecera Location:
/next-page/id=bF90aGVfd2F5X2FmNTFlMjNifQ==

3. Concatenar ambas cadenas codificadas en Base64 en orden de aparición:
YWNhZGVteTwtcm94aWVzX2FsbF90aGVfd2F5X2FmNTFlMjNifQ==

4. Decodificar la cadena resultante usando CyberChef (From Base64) o desde la terminal:
echo "YWNhZGVteTwtcm94aWVzX2FsbF90aGVfd2F5X2FmNTFlMjNifQ==" | base64 -d
```

```
academy{proxies_all_the_way_af51e23b}
```


## Notas adicionales

- Activar la casilla Keep log o (Conservar registro) para asi lograr capturar la petición original y seguir la cadena de redirecciones.

- Si una cadena de texto termina en = o == probablemente es Base 64.

## Referencias

https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=WVdOaFpHVnRlWHR3Y205NGFXVnpYMkZzYkY5MGFHVmZkMkY1WHpZMk1XWmpNems0ZlE9PQ