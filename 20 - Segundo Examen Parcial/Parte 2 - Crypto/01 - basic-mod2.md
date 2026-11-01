## Descripción

A new modular challenge! Download the message [here](https://challenge-files.cylabacademy.net/library/8493f8b1c07d84e858fa52d3dacdc63752275286da7a30b69fab36993eafb5ea/message.txt).

Take each number mod 41 and find the modular inverse for the result. Then map to the following character set: 1-26 are the alphabet, 27-36 are the decimal digits, and 37 is an underscore.

Wrap your decrypted message in the academy flag format (i.e. `academy{decrypted_message}`)

## Solución

```

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget https://challenge-files.cylabacademy.net/library/79ab2df83c3efdaa68f8d1d7b4ce3e478bd49e8193ca7002a30ea460743c412c/message.txt
--2026-10-30 23:15:16--  https://challenge-files.cylabacademy.net/library/79ab2df83c3efdaa68f8d1d7b4ce3e478bd49e8193ca7002a30ea460743c412c/message.txt
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 18.238.132.49, 18.238.132.115, 18.238.132.88, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|18.238.132.49|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 86 [application/octet-stream]
Saving to: ‘message.txt’

message.txt                   100%[=================================================>]      86  --.-KB/s    in 0s

2026-10-30 23:15:17 (37.9 MB/s) - ‘message.txt’ saved [86/86]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cat message.txt
309 44 274 149 57 378 313 311 64 420 405 86 98 195 256 48 238 277 448 411 240 436 214



Y = X^-1 (mod 41)

(X * Y)mod 41 = 1

... funcion de python 
pow(numero, -1, 41)

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ python
Python 3.14.7 (main, Sep  5 2026, 05:55:41) [GCC 16.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> pow(309, -1, 41)
28


equivalencia a nuesto alfabeto...
28 = 1

parte de la flago

1...

y haci se realizaria manualmente.


-- A cada numero calcularemos su inverso modular mod 41

-- Convertimos el resultado en una letra, número o guion bajo.

--asignamos el valor obenido a el alfabeto, numero, o guion... que corresponde
1 = A
2 = B
3 = C
4 = D
5 = E
6 = F
7 = G
8 = H
9 = I
10 = J
11 = K
12 = L
13 = M
14 = N
15 = O
16 = P
17 = Q
18 = R
19 = S
20 = T
21 = U
22 = V
23 = W
24 = X
25 = Y
26 = Z
27 = 0
28 = 1
29 = 2
30 = 3
31 = 4
32 = 5
33 = 6
34 = 7
35 = 8
36 = 9
37 = _



script--

archivo = open("message.txt", "r")
numeros = archivo.read().split()
archivo.close()

mensaje = ""

for numero in numeros:
    numero = int(numero)

    resultado = pow(numero, -1, 41)

    if resultado >= 1 and resultado <= 26:
        caracter = chr(resultado + 64)

    elif resultado >= 27 and resultado <= 36:
        caracter = str(resultado - 27)

    elif resultado == 37:
        caracter = "_"

    mensaje = mensaje + caracter

print("Mensaje:", mensaje)
print("Flag: academy{" + mensaje + "}")



┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ python3 resolver.py
```

```
academy{1NV3R53LY_H4RD_950D690F}
```

## Notas adicionales

## Referencias