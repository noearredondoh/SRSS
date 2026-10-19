## Descripción

In RSA d is a lot bigger than e, why don't we use d to encrypt instead of e?

## Solución

Se estableció una conexión con el servidor del reto, despues proporcionó los valores de `c`, `n` y `e`.Se identificó que el reto utilizaba el exponente privado `d` para cifrar el mensaje en lugar del exponente público habitual.

Para recuperar el mensaje original, se aprovechó esta configuración utilizando el valor común del exponente público `e = 65537`.

Se creó un script en Python llamado `rsa2.py` mediante el comando:
`nano rsa2.py`

En el programa se realizó la operación de exponenciación modular para descifrar el mensaje:
```
e = 65537
m = pow(c, e, n)
```

Posteriormente, se convirtió el resultado numérico a texto mediante:
```
mensaje = m.to_bytes((m.bit_length() + 7) // 8, "big")
print("Mensaje:", mensaje.decode(errors="replace"))
```

Finalmente, se ejecutó el programa:
`python3 rsa2.py`

Y obtuvimos la bandera
```
academy{bad_1d3a5_8722867}
```
## Notas adicionales

## Referencias