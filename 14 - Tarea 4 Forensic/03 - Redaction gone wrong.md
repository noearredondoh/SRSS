## Descripción

Now you DON’T see me. This [report](https://challenge-files.cylabacademy.net/library/455e6e9581a9272cf0cd6a8f2da0a7cdcfefdb52dc7a7f9c09a27705e2c94103/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?

## Solución

Se descargó el archivo `Financial_Report_for_ABC_Labs.pdf` y se analizó utilizando la herramienta `pdftotext`. Se ejecutó el siguiente comando:

```
pdftotext -layout Financial_Report_for_ABC_Labs.pdf -
```

Al extraer el contenido del documento, se identificó que parte de la información censurada con barras negras seguía siendo accesible, ya que únicamente había sido cubierta visualmente. Entre el texto recuperado se encontró la bandera del reto.

```
academy{C4n_Y0u_S33_m3_fully}
```
## Notas adicionales

`pdftotext` es una herramienta incluida en el paquete `poppler-utils` que permite extraer texto de archivos PDF. Es útil en análisis forenses para recuperar información que ha sido ocultada visualmente, pero que no fue eliminada del documento.

## Referencias