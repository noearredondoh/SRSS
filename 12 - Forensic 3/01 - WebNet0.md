## Descripción

We found this [packet capture](https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/webnet0-capture.pcap) and [key](https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/picopico.key). Recover the flag.

- Try using a tool like Wireshark.
- How can you decrypt the TLS stream?

## Solución

Se descargaron los archivos `webnet0-capture.pcap` y `picopico.key` y se abrió la captura con Wireshark:
```
wireshark webnet0-capture.pcap
```
Como el tráfico estaba cifrado con TLS, se ingresó a **Edit → Preferences → Protocols → TLS → RSA keys list** y se agregó `picopico.key` en el puerto `443` con protocolo `http`

Después se aplicó el filtro:
```
http
```

Esto permitió visualizar el tráfico HTTP descifrado. Finalmente, se seleccionó una respuesta **200 OK** y se utilizó **Follow → HTTP Stream** para encontrar la bandera

```
academy{nongshim.shrimp.crackers}
```

## Notas adicionales

## Referencias