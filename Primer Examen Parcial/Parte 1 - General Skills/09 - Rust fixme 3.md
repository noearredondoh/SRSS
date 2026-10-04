## Descripción

Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!

Download the Rust code [here](https://challenge-files.cylabacademy.net/library/6df8b7779faf29e53f515922041d99bc26381a332ca090c291ba20577ac7cf92/fixme3.tar.gz).

## Solución

Descargamos el archivo lo descomprimimos con el comando de abajo. Cuando lo descomprimimos nos movemos hasta encontrar main.rs y lo corremos con nano le pedi a la IA que verificara y existe un apartado de unsafe{ } que esta comentado, lo cual no deberia, editamos borramos //, guardamos y lo corremos nos movemos a donde estaban los archivos de cargo y lo corremos cargo run al tratar de correrlo me pidio instalar ciertas cosas escogi la que decia cargo +ubunto 1.75 o algo asi En Rust, cuando intentas usar punteros crudos (raw pointers) y acceder directamente a la memoria con funciones como `std::slice::from_raw_parts`, el compilador te obliga a envolver ese código dentro de un bloque **`unsafe { }`**. Si no lo haces, el código se niega a compilar.

Si revisas el archivo `main.rs`, notarás que las líneas que declaran el bloque `unsafe` fueron comentadas intencionalmente con. Tuve que pedirle ayuda a la Ia porque salian muchos errrores, me faltaba instalar muchas cosas pero al final se logro correr y obtener la bandera

```
academy{n0w_y0uv3_f1x3d_1h3m_411}
```

## Notas adicionales

tar -xzf fixme3.tar.gz en este comando la z es la que nos permite extrer del archivo .gz

## Referencias