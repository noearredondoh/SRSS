## Descripción

We received an encrypted message. The modulus is built from primes large enough that factoring them isn’t an option, at least not today. See if you can make sense of the numbers and reveal the flag. Download the [message](https://challenge-files.cylabacademy.net/library/c34366f2cc6000ab1b4b88ae999eb420e715b6f650e378bc6d586d6e859b7b35/message.txt)
## Solución

1. Se descargó el archivo `message.txt`, que contenía los valores del cifrado RSA: `n`, `e` y `c`.

2. Se identificó que el exponente público era `e = 20`, lo que sugería la posibilidad de realizar un ataque de exponente pequeño.

3. Se comprobó que la biblioteca `sympy` estaba instalada en Kali Linux.

4. Se creó un script llamado `solve.py` para leer los valores del archivo y calcular la raíz vigésima del mensaje cifrado mediante la función `integer_nthroot(c, e)`.

5. Al ejecutar el script, se obtuvo una raíz exacta, lo que permitió recuperar el mensaje original sin factorizar `n`.

6. Finalmente, se convirtió el resultado a texto, obteniendo la bandera del reto.
```
academy{t1ny_e_d6b18b0b}
```

## Notas adicionales

**Ataque de exponente pequeño en RSA:** Consiste en aprovechar situaciones donde el mensaje elevado al exponente público es menor que el módulo RSA. En estos casos, es posible recuperar el mensaje calculando directamente una raíz entera del texto cifrado, sin necesidad de factorizar el módulo.

## Referencias