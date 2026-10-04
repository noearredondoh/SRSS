## Descripción

Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!

Download the Rust code [here](https://challenge-files.cylabacademy.net/library/b9cfc84c442958b8ac848ddc0692bed9ef01a15877b8d37f36afbe68b5849acc/fixme1.tar.gz)

1. Cargo is Rust's package manager and will make your life easier. See the getting started page [here](https://doc.rust-lang.org/book/ch01-03-hello-cargo.html)
2. [println!](https://doc.rust-lang.org/std/macro.println.html)
3. Rust has some pretty great compiler error messages. Read them maybe?

## Solución

```
Primero se descargó el archivo proporcionado por el reto y se descomprimió utilizando:
**tar -xzf fixme1.tar.gz**

Después se ingresó a la carpeta del proyecto:
**cd fixme1**

Al intentar compilar el programa con:
**cargo build**

el compilador de Rust mostró tres errores en el archivo src/main.rs. Para corregirlos se abrió el archivo con:
**nano src/main.rs**

Se realizaron las siguientes correcciones: se agregó el ";" faltante al final de la declaración de "key", se cambió "ret;" por "return;" y se corrigió el formato de impresión de ":?" a "{:?}".

Después de guardar los cambios se volvió a compilar:
**cargo build**

Al no presentarse más errores, se ejecutó el programa con:
**cargo run**
```

```
academy{4r3_y0u_4_ru$t4c30n_n0w?}
```

## Notas adicionales

El compilador de Rust fue útil para resolver el reto, ya que indicaba la ubicación de cada error y proporcionaba pistas sobre cómo corregirlo. El objetivo principal era identificar y solucionar los errores de sintaxis presentes en el código.

## Referencias