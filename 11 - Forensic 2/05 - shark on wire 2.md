## Descripción

We found this [packet capture](https://challenge-files.cylabacademy.net/library/f76620763560ca0683be36e0ed4648743f969ab4d852fda0d8fb4d3ae21a173d/shark-on-wire-2-capture.pcap). Recover the flag that was pilfered from the network.

## Solución

```
Para resolver el reto se descargó el archivo de captura de red y se abrió con Wireshark. Se filtraron los paquetes UDP y se encontró tráfico sospechoso dirigido al puerto 22, por lo que se utilizó el filtro:

udp.dstport == 22

Se observó que los puertos de origen tenían valores como 5097, 5099, 5100, etc. Al restarles 5000, los resultados correspondían a códigos ASCII. Para automatizar la extracción y conversión se utilizó:

tshark -r shark-on-wire-2-capture.pcap -Y "udp.dstport == 22" -T fields -e udp.srcport | awk '{printf "%c", $1-5000}'

El comando tomó cada puerto de origen, le restó 5000 y convirtió el resultado a su carácter ASCII correspondiente, reconstruyendo así la flag completa del reto.
```

```
academy{p1LLf3r3d_data_v1a_st3g0}
```

## Notas adicionales

## Referencias

https://gemini.google.com/app?hl=es