## Descripción

We found this [packet capture](https://challenge-files.cylabacademy.net/library/e64f2c2aaf9bf531af7be1787c1407c47a4cc7b57f251d5108a1151e9721a2d6/shark-on-wire-1-capture.pcap). Recover the flag.

- Try using a tool like Wireshark, What are streams?

## Solución

```
Se abrió el archivo .pcap en Wireshark y se filtraron los paquetes utilizando el protocolo UDP. Después, con la opción **Follow → UDP Stream**, se revisaron los diferentes streams hasta encontrar el que contenía la flag
```

```
academy{StaT31355_636f6e6e}
```

## Notas adicionales

## Referencias