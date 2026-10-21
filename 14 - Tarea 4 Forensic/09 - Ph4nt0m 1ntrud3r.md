## Descripción

A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.

To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!

Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.cylabacademy.net/library/5806be215fe6052652521da2db517d6e0e1ce81392cc30d4ed8967825b2cf94c/myNetworkTraffic.pcap) and try to get the flag.

## Solución

Se descargó el archivo `myNetworkTraffic.pcap` y se analizó mediante Wireshark, identificando 22 paquetes TCP con marcas de tiempo desordenadas.

Posteriormente, se utilizó `tshark` para extraer los datos de los paquetes y ordenarlos cronológicamente. Se convirtieron los valores hexadecimales a texto con `xxd` y se decodificaron individualmente utilizando Base64 mediante el comando:

```
tshark -r myNetworkTraffic.pcap -T fields -e frame.time_epoch -e tcp.payload | sort -n | cut -f2 | while read hex; do echo "$hex" | xxd -r -p | base64 -d 2>/dev/null; done
```

Finalmente, entre los datos recuperados se identificó la bandera del reto.

```
academy{1t_w4snt_th4t_34sy_tbh_4r_a55faeed}
```

## Notas adicionales

`Wireshark` permite visualizar y analizar paquetes de red, mientras que `tshark` proporciona funciones similares desde la terminal. Ambas herramientas son útiles en análisis forenses para investigar tráfico sospechoso y recuperar información transmitida por la red.

## Referencias