## Descripción

Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.

Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/17/challenge.zip)

## Solución

```
NoeAH-academy@webshell:~$ ssh -p 50858 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:50858 ([18.217.83.136]:50858)' can't be established.
ED25519 key fingerprint is SHA256:M8hXanE8l/Yzfs8iuxNsuFL4vCzCKEIlM/3hpO13tfQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:50858' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Lower! Try again.
Enter your guess: 250
Higher! Try again.
Enter your guess: 375
Lower! Try again.
Enter your guess: 312
Lower! Try again.
Enter your guess: 281
Lower! Try again.
Enter your guess: 265
Lower! Try again.
Enter your guess: 257
Congratulations! You guessed the correct number: 257
Here's your flag: picoCTF{g00d_gu355_6dcfb67c}
Connection to atlas.picoctf.net closed.
```
## Notas adicionales

El reto requería adivinar un número secreto entre 1 y 1000 a través de una conexión `ssh`. Se aplicó el algoritmo de búsqueda binaria para ir dividiendo el rango de opciones exactamente a la mitad en cada intento, basándose en las respuestas _Higher_ o _Lower_ del servidor hasta acorralar el número y obtener la bandera

## Referencias