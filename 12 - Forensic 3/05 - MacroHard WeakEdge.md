## Descripción

I've hidden a flag in this file. Can you find it? [Forensics_is_fun.pptm](https://challenge-files.cylabacademy.net/library/ef35dfe613527d28fe872d94179b53bc1a0497ddecf57e51d160c910be3a8e8a/Forensics_is_fun.pptm)

## Solución

```
- Se analizó el archivo `Forensics_is_fun.pptm`, aprovechando que las presentaciones de Microsoft PowerPoint utilizan la especificación Office Open XML y funcionan internamente como contenedores ZIP comprimidos.
    
- Se extrajo la estructura de directorios del archivo ejecutando el comando `unzip Forensics_is_fun.pptm -d extraido` desde la terminal.
    
- Se inspeccionaron los recursos desempaquetados mediante el comando `find . -type f` para localizar elementos o rutas inusuales dentro del proyecto.
    
- Se identificó un archivo sospechoso nombrado `hidden` ubicado en la ruta `./ppt/slideMasters/hidden`.
    
- Al revisar el contenido del archivo con `cat`, se observó una cadena codificada en **Base64** con espacios intercalados entre los caracteres como método de ofuscación.
    
- Se eliminaron los espacios en blanco de la cadena utilizando el comando `tr -d ' '`.
    
- Se redirigió la salida limpia hacia la herramienta de decodificación ejecutando `base64 -d`.
    
- Se obtuvo como resultado la bandera
```

```
picoCTF{D1d_u_kn0w_ppts_r_z1p5}
```

## Notas adicionales

**Estructura Office Open XML:** Los documentos modernos de Microsoft Office (`.docx`, `.xlsx`, `.pptm`) siguen la especificación OpenXML. Cambiar la extensión a `.zip` o usar herramientas de descompresión permite inspeccionar directamente archivos XML, macros VBA (`vbaProject.bin`), imágenes y recursos embebidos.

## Referencias