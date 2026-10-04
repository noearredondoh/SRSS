## Descripción

There's a flag shop selling stuff, can you buy a flag? [Source](https://challenge-files.cylabacademy.net/library/c379a744fef22c0c9f3179034df9d627955bfeeac11416bc955a4661dd361ef2/store.c). Connect with `nc chatelaine.cylabacademy.net 44603`.

- Two's compliment can do some weird things when numbers get really big!
## Solución

```
1. Conectarse al servicio mediante netcat
nc chatelaine.cylabacademy.net 44603

2. Navegar en el menú para comprar banderas falsas
Selección de menú: 2 (Buy Flags) -> 1 (Definitely not the flag Flag)

3. Ingresar una cantidad lo suficientemente grande para desbordar el entero de 32 bits
Cantidad deseada: 3579138

4. Verificar que el saldo haya aumentado a más de mil millones de monedas
Selección de menú: 1 (Check Account Balance)

5. Comprar la flag real
Selección de menú: 2 (Buy Flags) -> 2 (1337 Flag) -> 1 (Cantidad)
```

```
academy{m0n3y_bag5_A25Fa481}
```

## Notas adicionales

## Referencias