## Descripción

This service provides you an encrypted flag. Can you decrypt it with just N & e?

## Solución

1. Se descargó y analizó el archivo `encrypt.py`, identificando cómo se generaban las claves RSA mediante los números primos `p` y `q`.

2. Se estableció una conexión con el servidor utilizando `nc`, obteniendo los valores `N`, `e` y `ciphertext`.

3. Se realizaron dos conexiones para obtener diferentes valores de `N` y analizar posibles vulnerabilidades.

4. Se creó un script en Python llamado `rsa_attack.py`, utilizando la función `gcd()` para calcular el máximo común divisor entre ambos módulos.

5. Se descubrió que los módulos compartían el factor primo `p = 2`, permitiendo calcular fácilmente el otro factor mediante `q = N // 2`.

6. Se calculó la función de Euler `φ(N) = (p-1)(q-1)` y posteriormente la clave privada `d`, utilizando el inverso modular.

7. Finalmente, se descifró el mensaje mediante `pow(c, d, N)` y se convirtió el resultado a texto, obteniendo la bandera.
```
academy{tw0_1$_pr!m3cfb893a9}
```
## Notas adicionales

**RSA:** Es un algoritmo de criptografía asimétrica que utiliza una clave pública para cifrar y una clave privada para descifrar información. Su seguridad depende de la dificultad de factorizar números muy grandes.

**Vulnerabilidad encontrada:** Uno de los factores del módulo RSA era `2`, lo que permitió factorizar `N` fácilmente y recuperar la clave privada.

## Referencias