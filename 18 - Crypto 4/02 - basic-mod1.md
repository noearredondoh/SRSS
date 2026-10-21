## Descripción

We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://challenge-files.cylabacademy.net/library/23b095a85da350dcda44aefdf5a62785a023f5d4570374d08eef71aefd096f7f/message.txt).

Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.

Wrap your decrypted message in the academy flag format (i.e. `academy{decrypted_message}`)

## Solución

- Se descargó el archivo `message.txt`, el cual contenía una serie de números que representaban un mensaje cifrado.

- Se analizaron las instrucciones del reto, identificando que era necesario aplicar la operación **módulo 37** a cada número para obtener su residuo.

- Se utilizó **Python** para crear un programa que leyera los números y aplicara la operación `% 37`.

- Se estableció una cadena de caracteres con las letras de la A a la Z (0–25), los dígitos del 0 al 9 (26–35) y el guion bajo (36).

- Mediante un ciclo `for`, se calculó el residuo de cada número y se convirtió al carácter correspondiente.

- Finalmente, se obtuvo el mensaje `R0UND_N_R0UND_81CE8A51`, el cual se colocó dentro del formato solicitado para obtener la bandera.
```
academy{R0UND_N_R0UND_81CE8A51}
```
## Notas adicionales

**Operación módulo:** Es una operación matemática que permite obtener el residuo de una división entera. En Python se representa mediante el operador `%`. Por ejemplo, `39 % 37 = 2`.
## Referencias