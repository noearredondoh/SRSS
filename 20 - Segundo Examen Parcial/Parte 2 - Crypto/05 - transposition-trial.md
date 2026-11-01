## Descripción

Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message. Download the corrupted message [here](https://challenge-files.cylabacademy.net/library/304dc08e455ad3c33cf532bb41f44a7e939e8e2ad161d9c9012b8375dee48829/message.txt)

## Solución

```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ ls

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget https://challenge-files.cylabacademy.net/library/304dc08e455ad3c33cf532bb41f44a7e939e8e2ad161d9c9012b8375dee48829/message.txt
--2026-10-31 00:23:47--  https://challenge-files.cylabacademy.net/library/304dc08e455ad3c33cf532bb41f44a7e939e8e2ad161d9c9012b8375dee48829/message.txt
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 18.238.132.26, 18.238.132.115, 18.238.132.49, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|18.238.132.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 54 [application/octet-stream]
Saving to: ‘message.txt’

message.txt                            100%[==========================================================================>]      54  --.-KB/s    in 0s

2026-10-31 00:23:48 (21.3 MB/s) - ‘message.txt’ saved [54/54]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cat message.txt
heTfl g as icaaemd{7y4NRP051N5_16_35P3X51N3_V1CCA2B2}A



...

...

...

psicion 
1 2 3

camiarla a 
3 1 2

ejemplo los primeros 3 caracteres... que fue el que me parecio un the, y haci fue
1 = heT

1=h 2=e 3=T

3=T 1=h 2=e

 = The 


2 = "fl " contamos espacios como carateres...
=" fl"

3 = g a
="ag "

4 ="s i"
="is "

5 ="caa" 
="aca"

6="emd"
"dem"

7="{7y"
="y{7"

8="4NR"
="R4N"

9="P05"
="5P0"

10="1N5"
="51N"

11="_16"
="6_1"

12="_35"
="5_3"

13="P3X"
="XP3"

14="51N"
="N51"

14="3_V"
="V3_"

15="1CC"
="C1C"

16="A2B"
="BA2"

17="2}A"
="A2}"


academy{7R4N5P051N6_15_3XP3N51V3_C1CBA2A2}

```

```
academy{7R4N5P051N6_15_3XP3N51V3_C1CBA2A2}
```
## Notas adicionales

## Referencias