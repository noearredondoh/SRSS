## Descripción

I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.cylabacademy.net/library/4fc4d3051e630688372636e3f3922caf22e1edb92ab59b085c18897bebefd511/whitepages.txt) is all blank!

- There is data encoded somewhere... there might be an online decoder.

## Solución

```
Para resolver el reto, primero se descargó el archivo whitepages.txt, el cual parecía estar vacío. Para comprobar si contenía información oculta, se utilizó el comando cat -A whitepages.txt, con el que se detectaron caracteres que normalmente no eran visibles. Después se identificó que el archivo utilizaba dos tipos de espacios diferentes: un espacio Unicode \u2003 (EM SPACE) y un espacio normal. Estos caracteres representaban información en código binario, por lo que mediante un pequeño programa en Python se sustituyó el espacio Unicode por 0 y el espacio normal por 1. Finalmente, los bits obtenidos se agruparon en bloques de 8 y se convirtieron a caracteres, revelando el mensaje oculto y la flag del reto.
```

```
academy{not_all_spaces_are_created_equal_6cf6e66c300333a311200c7fb25e14c9}
```

## Notas adicionales

## Referencias