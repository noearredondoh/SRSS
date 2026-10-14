## Descripción

Class, take your seats! It's PRIME-time for a quiz..

## Solución

Se resolvio este reto utilizando las fórmulas correspondientes y Python para realizar los cálculos con números grandes. Finalmente, se convirtió el último `plaintext` a hexadecimal y posteriormente a ASCII, obteniendo la bandera del reto.

```
RSA - llave publica - asimetrico
-------------------------------------------------------------------------
m   - mensaje original o mensaje en texto plano 
c   - mensaje cifrado (ciphertext)
p,q - son dos numeros primos distintos y muy grandes
n   - es el modulo (lo compartes las llaves publica como privada)
tn  - totient n (funcion de euler)
e   - llave public - 65537 (exponente)  2 ^ 16 + 1
d   - llave privada

Calculos
--------------------------------------------------
n  = p * q
tn = (p -1) * (q-1)
d = e ^ -1 (mod tn)	- pow(e, -1, tn)

Cifrar  
--------------------------------------------------
c = m ^ e (mod n)	- pow(m, e, n)

Decifrars
--------------------------------------------------
m = c ^ d (mod n)	- pow(c, d, n)
```

```
academy{wA8_th4t$_ill3aGal..od365BFb2}
```

## Notas adicionales

RSA es un algoritmo de criptografía asimétrica que utiliza una clave pública para cifrar y una clave privada para descifrar información. Su seguridad se basa en la dificultad de factorizar números muy grandes en sus factores primos.
## Referencias

https://simple.wikipedia.org/wiki/RSA_algorithm