## Descripción

We found this [packet capture](https://challenge-files.cylabacademy.net/library/afb7599dd63cad30a04eb98d0e4057608120371eb3e8943b632505e32c8b622c/webnet1-capture.pcap) and [key](https://challenge-files.cylabacademy.net/library/afb7599dd63cad30a04eb98d0e4057608120371eb3e8943b632505e32c8b622c/picopico.key). Recover the flag.

- Try using a tool like Wireshark.
- How can you decrypt the TLS stream?

## Solución

1. Se descargaron los archivos correspondientes a la captura de red (`packet capture`) y la llave criptográfica (`key`) proporcionados en la plataforma del reto.

2. Se abrió el archivo de captura en la herramienta Wireshark. Al observar que el tráfico web estaba cifrado mediante el protocolo TLS, se procedió a vulnerar esta capa de seguridad de la misma forma que en el reto anterior.

3. Se cargó la llave privada (`key`) en las configuraciones de Wireshark (`Edit` -> `Preferences` -> `Protocols` -> `TLS` -> "RSA keys list") para habilitar el descifrado pasivo del tráfico interceptado.

4. Una vez que los paquetes HTTP fueron descifrados y revelados en texto claro, se inspeccionó el flujo de datos y se identificó la descarga de un archivo de imagen desde el servidor.

5. Se utilizó la funcionalidad de extracción de Wireshark (`File` -> `Export Objects` -> `HTTP`) para guardar la imagen transmitida localmente en el equipo.

6. Posteriormente, se ejecutó la herramienta de línea de comandos `exiftool` sobre la imagen extraída para analizar a profundidad todos sus metadatos.

7. Al revisar la salida de `exiftool`, se localizó la bandera del reto, la cual había sido inyectada intencionalmente dentro de uno de los campos de texto de los metadatos de la imagen.


```
academy{honey.roasted.peanuts}
```
## Notas adicionales

## Referencias