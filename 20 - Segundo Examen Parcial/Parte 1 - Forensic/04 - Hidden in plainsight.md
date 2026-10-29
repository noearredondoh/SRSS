## Descripción

You’re given a seemingly ordinary JPG image. Something is tucked away out of sight inside the file. Your task is to discover the hidden payload and extract the flag. Download the jpg image [here](https://challenge-files.cylabacademy.net/library/364c5c391edaf4ab3da852e0fc51a5285bc4a570900618b112c52805fc1d5c14/img.jpg)

1. Download the jpg image and read its metadata
## Solución

1. Descargar la imagen 
2. Usar exiftool img.jpg 
3. Al ver en los datos observamos que existe el comentario cifrado en base 64 asi que lo decodificamos con: echo "c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9" | base64 -d El resultado es steghide:cEF6endvcmQ= que nos indica el lugar y la contraseña para acceder a el. 
4. Utilizamos steghide extract -sf img.jpg y cuando se nos pida la contraseña la ingresamos. 
5. Utilizamos lo siguiente para obtener la bandera.
```
echo "cEF6endvcmQ=" | base64 -d # -> pAzzword 
steghide extract -sf img.jpg -p pAzzword 
cat flag.txt
```

```
academy{h1dd3n_1n_1m4g3_45cfe9c1}
```
## Notas adicionales

## Referencias