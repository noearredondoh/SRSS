## Descripción

In RSA, a small e value can be problematic, but what about N? Can you decrypt this?

## Solución

Se descargó el archivo `values`, que contenía los valores de `n`, `e` y el mensaje cifrado (`c`). Se visualizó su contenido mediante el comando:
`cat values`

Se identificó que el módulo `n` era relativamente pequeño, por lo que se utilizó la herramienta FactorDB para factorizarlo y obtener los números primos `p` y `q`.

Posteriormente, se creó un script en Python llamado `rsa.py`:
`nano rsa.py`

En el programa se calculó la función totiente de Euler y la clave privada `d`, utilizando las siguientes operaciones:
```python
tn = (p - 1) * (q - 1)
d = pow(e, -1, tn)
m = pow(c, d, n)
```

Después, se convirtió el mensaje descifrado a texto y se invirtió su contenido para recuperar la bandera:
```python
mensaje = m.to_bytes((m.bit_length() + 7) // 8, "big")
print("Bandera:", mensaje.decode()[::-1])
```

Finalmente, se ejecutó el programa mediante:
`python3 rsa.py`

Obteniendo la bandera:
```
academy{smal11_N_n0_g0od_a3ac7152}
```

## Notas adicionales

## Referencias

https://factordb.com/
