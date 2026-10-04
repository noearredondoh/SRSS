## Descripción

Play this short game to get familiar with terminal applications and some of the most important rules in scope for picoCTF. Connect to the program with netcat:

$ nc xebec.cylabacademy.net 34302

- When a choice is presented like [a/b/c], choose one, for example: `c` and then press Enter.

## Solución

```
1. Conectarse al juego de simulación mediante netcat
nc xebec.cylabacademy.net 34302

2. Avanzar en la narrativa interactiva presionando [Enter]

3. Responder las preguntas de opción múltiple según las reglas de picoCTF:
- ¿Registro de cuenta?: c (Register a single, private account)
- ¿Acción en el reto?: a (Play the game)

4. Completar las preguntas restantes del flujo interactivo para obtener la flag al final
```

```
academy{m1113n1um_3d1710n_401821da}
```

## Notas adicionales

El reto simula una aventura de texto (_interactive fiction_) ejecutada sobre una conexión en red. La interacción requiere avanzar la historia mediante entradas vacías (`Enter`) y responder a menús de opción múltiple con la letra correspondiente.

## Referencias