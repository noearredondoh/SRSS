## Descripción

My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/179/challenge.zip)

## Solución

```
NoeAH-academy@webshell:~$ wget https://artifacts.picoctf.net/c_titan/179/challenge.zip
--2026-08-30 04:41:08--  https://artifacts.picoctf.net/c_titan/179/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.95, 3.160.5.40, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 24648 (24K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                              100%[========================================================================================================================================>]  24.07K  --.-KB/s    in 0.004s  

2026-08-30 04:41:08 (5.76 MB/s) - 'challenge.zip' saved [24648/24648]

NoeAH-academy@webshell:~$ unzip challenge.zip
Archive:  challenge.zip
   creating: drop-in/
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
  inflating: drop-in/.git/refs/heads/main  
   creating: drop-in/.git/refs/heads/feature/
 extracting: drop-in/.git/refs/heads/feature/part-1  
 extracting: drop-in/.git/refs/heads/feature/part-2  
 extracting: drop-in/.git/refs/heads/feature/part-3  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/77/
 extracting: drop-in/.git/objects/77/d6ceca6fe23b57d88cf16f20003e10d6715690  
   creating: drop-in/.git/objects/b9/
 extracting: drop-in/.git/objects/b9/32e8c048154a46d224cd7691c99dc8cb88164a  
   creating: drop-in/.git/objects/5e/
 extracting: drop-in/.git/objects/5e/4b2dae1868abb644627483c78a683286dfe67c  
   creating: drop-in/.git/objects/6e/
 extracting: drop-in/.git/objects/6e/17fb3a35364b4f9bb8bef8b5e6a5af2d3e7dfa  
   creating: drop-in/.git/objects/43/
 extracting: drop-in/.git/objects/43/e44dd37ba0c0adc3d78d0b85d699859ec8d75c  
   creating: drop-in/.git/objects/30/
 extracting: drop-in/.git/objects/30/0cff1bf1f64637dd9ff603d90176e8e8bdeb01  
   creating: drop-in/.git/objects/7a/
 extracting: drop-in/.git/objects/7a/b4e25c0cd108374b2275fdb1fcdf635e591833  
   creating: drop-in/.git/objects/d1/
 extracting: drop-in/.git/objects/d1/f3407cee4479c075997b497fa290ca636fe258  
   creating: drop-in/.git/objects/74/
 extracting: drop-in/.git/objects/74/989a4f650d024929388b6788d2b4c214a07e49  
   creating: drop-in/.git/objects/c3/
 extracting: drop-in/.git/objects/c3/1215218d31567374eeed51505972af2ed46a37  
   creating: drop-in/.git/objects/04/
 extracting: drop-in/.git/objects/04/ebe96db2885e1a7af6d1e4ca7ce9b89e5ba743  
   creating: drop-in/.git/objects/12/
 extracting: drop-in/.git/objects/12/c2ae89d8035b7a5aa7cd169dc9e93cc68201be  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/main  
   creating: drop-in/.git/logs/refs/heads/feature/
  inflating: drop-in/.git/logs/refs/heads/feature/part-1  
  inflating: drop-in/.git/logs/refs/heads/feature/part-2  
  inflating: drop-in/.git/logs/refs/heads/feature/part-3  
  inflating: drop-in/flag.py         
NoeAH-academy@webshell:~$ cd drop-in
NoeAH-academy@webshell:~/drop-in$ git branch -a
NoeAH-academy@webshell:~/drop-in$ git checkout feature/part-1
Switched to branch 'feature/part-1'
NoeAH-academy@webshell:~/drop-in$ ls
flag.py
NoeAH-academy@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')NoeAH-academy@webshell:~/drop-in$ git checkout feature/part-2
Switched to branch 'feature/part-2'
NoeAH-academy@webshell:~/drop-in$ ls
flag.py
NoeAH-academy@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')NoeAH-academy@webshell:~/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
NoeAH-academy@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")

print("w0rk_798f9981}")
```

```
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_798f9981}
```
## Notas adicionales

La bandera estaba dividida en tres ramas del repositorio. Se utilizó `git branch -a` para descubrirlas y `git checkout` para entrar a cada una (`part-1`, `part-2` y `part-3`). Al leer el archivo `flag.py` con el comando `cat` dentro de cada rama, se extrajeron los tres fragmentos necesarios para ensamblar la bandera manualmente.

## Referencias