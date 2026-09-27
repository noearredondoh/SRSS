## Descripción

Do you know how to use the web inspector? Start searching [here](http://xebec.cylabacademy.net:11095/) to find the flag
## Solución

```
Se inspeccionó el código fuente de la página (about.html) y se identificó un atributo personalizado llamado "notify_true"

Se introdujo la cadena codificada en CyberChef aplicando la receta **From Base64** para convertir los datos a texto plano y se obtuvo la flag
```

```
academy{web_succ3ssfully_d3c0ded_e0ea179a}
```

## Notas adicionales

## Referencias

https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=WVdOaFpHVnRlWHQzWldKZmMzVmpZek56YzJaMWJHeDVYMlF6WXpCa1pXUmZaVEJsWVRFM09XRjk