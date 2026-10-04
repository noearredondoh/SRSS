## Descripción

Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.

The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden.

## Solución

Primero, nos dirigimos al apartado **#APIDocumentation**. En la página a la que somos redirigidos, bajamos hasta el final hasta encontrar la opción **GET**. La seleccionamos y después hacemos clic en **Try it out** para habilitar la ejecución. Finalmente, ejecutamos la petición y observamos la respuesta obtenida.

```
http://chatelaine.cylabacademy.net:46920/heapdump

podemos bajar el archivo en la consola con el siguiente comanddo...

wget http://chatelaine.cylabacademy.net:46920/heapdump -O (ingresa_nombre).heapsnapshot



O bien bajarlo desde el enlase de la pagina web, y con string y grep buscamos la bandera.
└─$ strings heapdump-1791003619846.heapsnapshot | grep "academy{"
academy{Pat!3nt_15_Th3_K3y_abc961cc}

```

```
academy{Pat!3nt_15_Th3_K3y_cc0f4fda}
```

## Notas adicionales

## Referencias