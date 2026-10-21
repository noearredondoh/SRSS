## Descripción

How about we take you on an adventure on exploring certificate signing requests Take a look at this CSR file [here](https://challenge-files.cylabacademy.net/library/adc86ad64fdfdb57ccdc30281c4c93aa2a8a913259426681737dc7e69d257275/readmycert.csr)

## Solución

- Se descargó el archivo `readmycert.csr`, el cual contenía una solicitud de firma de certificado digital (CSR).

- Se analizaron las pistas del reto, identificando que era necesario leer la información almacenada dentro del certificado.

- Se utilizó la herramienta **OpenSSL** en Kali Linux para examinar el contenido del archivo.

- Se ejecutó el comando `openssl req -in readmycert.csr -text -noout`, el cual permitió visualizar la información del CSR en formato legible.

- Se revisó el campo **Subject**, específicamente el atributo `CN` (Common Name), donde se encontraba la bandera.

- Finalmente, se identificó y extrajo la bandera solicitada.
```
academy{read_mycert_1767ceb4}
```

## Notas adicionales

**OpenSSL:** Es una herramienta de código abierto utilizada para trabajar con certificados digitales, claves criptográficas y protocolos de seguridad. Permite generar, analizar y verificar certificados.

**CSR (Certificate Signing Request):** Es una solicitud de firma de certificado que contiene información de la entidad solicitante y su clave pública.

**Common Name (CN):** Es un atributo del campo Subject que permite identificar al sujeto de un certificado digital. En este reto contenía la bandera oculta.

## Referencias