## Descripción

The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?

Download the Rust code [here](https://challenge-files.cylabacademy.net/library/048c73621a97b98cde18eae5a9495279f2396cb64c65235bb310e7ad26d726ac/fixme2.tar.gz).

[https://doc.rust-lang.org/book/ch04-02-references-and-borrowing.html](https://doc.rust-lang.org/book/ch04-02-references-and-borrowing.html)

## Solución

```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget https://challenge-files.cylabacademy.net/library/048c73621a97b98cde18eae5a9495279f2396cb64c65235bb310e7ad26d726ac/fixme2.tar.gz
--2026-10-03 21:56:11--  https://challenge-files.cylabacademy.net/library/048c73621a97b98cde18eae5a9495279f2396cb64c65235bb310e7ad26d726ac/fixme2.tar.gz
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.37, 13.226.187.22, 13.226.187.40, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.37|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1720 (1.7K) [application/octet-stream]
Saving to: ‘fixme2.tar.gz’

fixme2.tar.gz                 100%[=================================================>]   1.68K  --.-KB/s    in 0.005s

2026-10-03 21:56:12 (364 KB/s) - ‘fixme2.tar.gz’ saved [1720/1720]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ ls
fixme2.tar.gz

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ tar -xzf fixme2.tar.gz

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cd fixme2

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/fixme2]
└─$
┌──(jeex㉿LAPTOP-77F4GRAK)-[~/fixme2]
└─$ nano src/main.rs

/////////////////////////////////////////////////////////////////////////////
cambios
--fn decrypt(encrypted_buffer: Vec<u8>, borrowed_string: &String) {

nuevo -fn decrypt(encrypted_buffer: Vec<u8>, borrowed_string: &mut String) {

--let party_foul = String::from("Using memory unsafe languages is a: ");
nuevo-let mut party_foul = String::from("Using memory unsafe languages is a: ");


--decrypt(encrypted_buffer, &party_foul);
nuevo-decrypt(encrypted_buffer, &mut party_foul);

/////////////////////////////////////////////////////////////////////////////

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/fixme2]
└─$ cargo run
   Compiling crossbeam-utils v0.8.20
   Compiling rayon-core v1.12.1
   Compiling either v1.13.0
   Compiling crossbeam-epoch v0.9.18
   Compiling crossbeam-deque v0.8.5
   Compiling rayon v1.10.0
   Compiling xor_cryptor v1.2.3
   Compiling rust_proj v0.1.0 (/home/jeex/fixme2)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 11.60s
     Running `target/debug/rust_proj`
Using memory unsafe languages is a: PARTY FOUL! Here is your flag: academy{4r3_y0u_h4v1n5_fun_y31?}
```

```
academy{4r3_y0u_h4v1n5_fun_y31?}
```
## Notas adicionales

## Referencias