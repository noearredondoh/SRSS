## Descripción

Can you abuse the oracle?

An attacker was able to intercept communications between a bank and a fintech company. They managed to get the [message](https://challenge-files.cylabacademy.net/library/1b39f2751ae1461b00924da90f25e9803b0cee634d2244dccf6554277057994e/secret.enc) (ciphertext) and the [password](https://challenge-files.cylabacademy.net/library/1b39f2751ae1461b00924da90f25e9803b0cee634d2244dccf6554277057994e/password.enc) that was used to encrypt the message.

## Solución

```

- Se descargaron los artefactos `chall.py` y `output.txt`. Los datos revelan dos criptogramas ($c_1, c_2$), el módulo $N$, un exponente pequeño $e=17$ y la diferencia numérica exacta entre los mensajes planos: $m_1 - m_2 = -3$, lo que establece la relación $m_2 = m_1 + 3$.
    
- **Criptoanálisis (Ataque de Franklin-Reiter):**
    
    - Cifrar dos mensajes relacionados algebraicamente bajo el mismo módulo $N$ permite extraer el mensaje original calculando el Máximo Común Divisor (MCD) de dos polinomios en $\mathbb{Z}_N$:
        
        $$f_1(x) = x^{17} - c_1 \pmod N$$
        
        $$f_2(x) = (x + 3)^{17} - c_2 \pmod N$$
        
    - La raíz común de ambos polinomios es el mensaje $m_1$, por lo que su MCD resulta en el polinomio lineal $x - m_1$.
        
- **Corrección del Error Tipográfico:**
    
    - El MCD recuperó el primer mensaje $m_1$: `academy{m3ssage_w1th_typ0z`.
        
    - Como indica la descripción, el primer mensaje contenía un error. El mensaje corregido $m_2$ equivale a $m_1 + 3$. Al sumar 3 al valor ASCII del último carácter `z` (122), se obtiene 125, correspondiente al carácter `}`.
```

```
academy{su((3ss_(r@ck1ng_r3@_6e3fffd9}
```
## Notas adicionales

- **Vulnerabilidad de Mensajes Relacionados:** El ataque de Franklin-Reiter demuestra que RSA puro (Textbook RSA) es inseguro. Reenviar un mensaje tras corregir un simple error tipográfico compromete el criptosistema y permite la recuperación del texto claro en tiempo polinomial.
## Referencias
- Reto: picoCTF 2026 - Cryptography (Medium).
- Autor: Philip Thayer.