## Descripción

- Decrypt this message. Message: [message](https://challenge-files.cylabacademy.net/library/eb4325fac37933de66857090e6c78c226267394ccaf5c079ff593e3e33b4b95a/data.enc)
## Solución

1- Análisis del archivo:
Al inspeccionar el contenido del archivo cifrado se obtiene la estructura inicial del mensaje:

```
academy{crossingtherubiconvfuyazrb}
```
El prefijo `academy{` y el cierre `}` se mantienen en claro, por lo que únicamente el contenido encerrado dentro de las llaves (`xmjnndiboczmpwdxjiqaptvumw`) fue procesado con el desplazamiento alfabético.

2- Ataque por fuerza bruta (Fuerza Bruta de Desplazamiento):
Dado que el cifrado César solo cuenta con 26 desplazamientos posibles en el alfabeto inglés, se implementó un script en Python para probar todas las rotaciones posibles (0 a 25):

```python
cipher = "xmjnndiboczmpwdxjiqaptvumw"

for shift in range(26):
    plain = "".join(chr((ord(c) - 97 - shift) % 26 + 97) for c in cipher)
    print(f"Shift {shift:2d}: academy{{{plain}}}")
```

3-  Obtención del texto claro:
Al ejecutar la iteración, el desplazamiento **Shift 21** revela la frase coherente en inglés _"crossing the rubicon"_ seguida de su respectivo relleno:

```
Shift 21: academy{crossingtherubiconvfuyazrb}
```

## Notas adicionales

**Cifrado César:** Es una técnica de cifrado por sustitución que consiste en desplazar cada letra un número fijo de posiciones dentro del abecedario. Su nombre proviene de Julio César, quien utilizaba este método para proteger sus mensajes.
## Referencias