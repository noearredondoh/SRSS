## Descripción

Cookie Monster has hidden his top-secret cookie recipe somewhere on his website. As an aspiring cookie detective, your mission is to uncover this delectable secret. Can you outsmart Cookie Monster and find the hidden recipe?

## Solución

```
1. Inspeccionar las cookies guardadas en el navegador mediante Cookie-Editor o DevTools
Se identifica la cookie con el nombre: secret_recipe
Valor obtenido: YWNhZGVteXtjMDBrMWVfbTBuc3Rcl9sMHZlc19jMDBraWVzXzVBRUI1OTJffQ%3D%3D

2. Decodificar el valor mediante CyberChef o la terminal (URL Decode + Base64 Decode):
echo "YWNhZGVteXtjMDBrMWVfbTBuc3Rcl9sMHZlc19jMDBraWVzXzVBRUI1OTJffQ==" | base64 -d
```

```
academy{c00k1e_m0nster_l0ves_c00kies_5AEB592E}
```

## Notas adicionales

## Referencias

https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=WVdOaFpHVnRlWHRqTURCck1XVmZiVEJ1YzNSbGNsOXNNSFpsYzE5ak1EQnJhV1Z6WHpWQlJVSTFPVEpGZlElM0QlM0Q&oeol=CR