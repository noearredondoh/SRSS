## Descripción

How well can you perfom basic binary operations?

## Solución

```
NoeAH-academy@webshell:~$ nc titan.picoctf.net 56556

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 11101010
Binary Number 2: 01100001


Question 1/6:
Operation 1: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 111010
Incorrect. Try again
Enter the binary result: 01100000
Correct!

Question 2/6:
Operation 2: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11101011
Correct!

Question 3/6:
Operation 3: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 101100010101010
Correct!

Question 4/6:
Operation 4: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 101001011
Correct!

Question 5/6:
Operation 5: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 111010100
Correct!

Question 6/6:
Operation 6: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 00110000
Correct!

Enter the results of the last operation in hexadecimal: 30

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_6862762d}
```

## Notas adicionales

Se utilizó `nc` para establecer la conexión con el servidor del reto y CyberChef como herramienta de apoyo para realizar las conversiones y comprobar los resultados. Fue importante identificar correctamente cada operación y proporcionar las respuestas en el formato solicitado para finalmente obtener la flag.

## Referencias

https://gchq.github.io/CyberChef/