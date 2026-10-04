## Descripción

Why search for the flag when I can make a bookmarklet to print it for me? Browse [here](http://chatelaine.cylabacademy.net:27289/), and find the flag!

## Solución

```
1. Abrir la consola de desarrollador del navegador (F12) en la página del reto
2. Copiar y ejecutar el código JavaScript proporcionado en el bookmarklet:

javascript:(function() {
    var c = "picoCTF{bdkmrklet_skr1pt1ng_..."; // Cadena obfuscada/definida en el script
    alert(c);
})();
```

```
academy{p@g3_turn3r_a02192a2}
```

## Notas adicionales

**Bookmarklets:** Un _bookmarklet_ es un marcador de navegador que, en lugar de abrir una dirección URL tradicional, contiene una función ejecutadora de JavaScript que empieza con el esquema javascript:

## Referencias