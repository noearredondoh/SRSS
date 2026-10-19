## Descripción

What happens if you have a small exponent? There is a twist though, we padded the plaintext so that (M∗∗e)(M∗∗e) is just barely larger than NN. Let's decrypt this: [values](https://challenge-files.cylabacademy.net/library/28a2479cff9eab20837067152fcead0a079e378b38249280192aef28a975269a/values)

## Solución

Se descargó el archivo `values`, el cual contenía los valores de `N`, `e = 3` y el mensaje cifrado (`ciphertext`).

Se identificó que el reto utilizaba un exponente público pequeño, por lo que se aplicó un ataque conocido como _Small Exponent Attack_, utilizando la fórmula:
**m = ∛(c + k × N)**

Para realizar los cálculos, se creó un script en Python llamado `mini_rsa.py` 

El programa calculó raíces cúbicas enteras, probando diferentes valores de `k` hasta encontrar una raíz exacta. Posteriormente, se convirtió el resultado a texto mediante:
`mensaje = m.to_bytes((m.bit_length() + 7) // 8, "big")`

Finalmente, se ejecutó el programa con el comando:
`python3 mini_rsa.py`

Se encontró `k = 0` y se recuperó el mensaje descifrado, obteniendo la bandera:
```
academy{e_sh0uld_b3_lArg3r_35f26e1a}
```

## Notas adicionales

El _Small Exponent Attack_ aprovecha el uso de exponentes públicos pequeños en RSA, como `e = 3`, cuando el mensaje no cuenta con un relleno criptográfico seguro. En este reto se utilizó Python para calcular raíces cúbicas enteras sin perder precisión.

## Referencias