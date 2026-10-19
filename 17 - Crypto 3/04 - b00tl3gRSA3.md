## Descripción

Why use p and q when I can use more?

## Solución

Se estableció una conexión con el servidor, despues  proporcionó los valores de `c`, `n` y `e = 65537`. Se identificó que, a diferencia del RSA tradicional, el módulo `n` estaba compuesto por múltiples factores primos.

Para factorizar el módulo se utilizó la herramienta Alpertron, donde también se calculó la función totiente de Euler mediante `Totient(n)`.

Posteriormente, se creó un script en Python llamado `rsa3.py`:
`nano rsa3.py`

En el programa se calculó la clave privada `d` y se descifró el mensaje mediante las siguientes operaciones:
```
e = 65537
d = pow(e, -1, tn)
m = pow(c, d, n)
```

Después, se convirtió el resultado numérico a texto utilizando:
```
mensaje = m.to_bytes((m.bit_length() + 7) // 8, "big")
print("Mensaje:", mensaje.decode(errors="replace"))
```

Finalmente, se ejecutó el programa:
`python3 rsa3.py`

Obteniendo la bandera:
```
academy{too_many_fact0rs_5984067}
```

## Notas adicionales

Este reto utiliza una variante de RSA conocida como _Multi-prime RSA_, en la que el módulo `n` se forma multiplicando más de dos números primos. Para calcular correctamente la clave privada, es necesario considerar todos los factores primos al obtener la función totiente de Euler.

## Referencias

https://www.alpertron.com.ar/ECMC.HTM