## Descripción

A message has been encrypted using RSA. The public key is gone… but someone might have been careless with the private key. Can you recover it and decrypt the message? Download the [flag](https://challenge-files.cylabacademy.net/library/9158482a92a4408128c3c320458089d0e8c2c1d8d8120ddaaabdf90397e4cedb/flag.enc) and [image](https://challenge-files.cylabacademy.net/library/9158482a92a4408128c3c320458089d0e8c2c1d8d8120ddaaabdf90397e4cedb/image.jpg).
## Solución

```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget https://challenge-files.cylabacademy.net/library/43fe409039addd5ea8db54dde7c2716afeaaac4275047cbfb23f6d5f81fb3ba4/flag.enc
--2026-10-30 23:45:18--  https://challenge-files.cylabacademy.net/library/43fe409039addd5ea8db54dde7c2716afeaaac4275047cbfb23f6d5f81fb3ba4/flag.enc
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 18.238.132.49, 18.238.132.88, 18.238.132.115, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|18.238.132.49|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 256 [application/octet-stream]
Saving to: ‘flag.enc’

flag.enc                      100%[=================================================>]     256  --.-KB/s    in 0s

2026-10-30 23:45:19 (123 MB/s) - ‘flag.enc’ saved [256/256]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget https://challenge-files.cylabacademy.net/library/43fe409039addd5ea8db54dde7c2716afeaaac4275047cbfb23f6d5f81fb3ba4/image.jpg
--2026-10-30 23:45:30--  https://challenge-files.cylabacademy.net/library/43fe409039addd5ea8db54dde7c2716afeaaac4275047cbfb23f6d5f81fb3ba4/image.jpg
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 18.238.132.49, 18.238.132.26, 18.238.132.115, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|18.238.132.49|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 20794 (20K) [application/octet-stream]
Saving to: ‘image.jpg’

image.jpg                     100%[=================================================>]  20.31K  --.-KB/s    in 0s

2026-10-30 23:45:31 (151 MB/s) - ‘image.jpg’ saved [20794/20794]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ ls
flag.enc  image.jpg

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ ls
flag.enc  image.jpg

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cat flag.enc
����ɸ�J��m��D�]�3��␦:���OX,�_��փ4뛉QYFH�h�Q��,�,��k<��kV�5�������Y�;�$>�B�p;q�jO��0F���H�|�iU�.���ϊ���|,`8��a�D]��3�q�+�j>�V�l�����(�lZ����(z�(��u�Q��hPq��g�;�Elˮ]�bv/վI��TSgr��m9�oa��5��af/�%��}|3��o�Q��    `�O�cm;_�C���
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ open image.jpg

... la pista menciona que los metadatos pueden ayudar.

```

```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ exiftool image.jpg
ExifTool Version Number         : 13.55
File Name                       : image.jpg
Directory                       : .
File Size                       : 21 kB
File Modification Date/Time     : 2026:09:23 01:00:30-06:00
File Access Date/Time           : 2026:10:30 23:47:56-06:00
File Inode Change Date/Time     : 2026:10:30 23:45:31-06:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Comment                         : 2d2d2d2d2d424547494e2050524956415445204b45592d2d2d2d2d0a4d494945765149424144414e42676b71686b6947397730424151454641415343424b63776767536a41674541416f49424151444e4247583339685161664f525a0a7a3147306c4a37697a48786c4556686e3964334562656c585158326770736a666a53654457517a4469775a464f3545524538467a567a6c3147685163636f67520a466f4948344b644b7871657a636a7069462f706572487653426442372f76586f3144796642517475464c7778426d54592b52622f6e39505674756a6f4b6f654a0a7765793864356b34542b6675775535724b39516776732b705377735436376377727a4b426b713046756a757237774873485771545561764564444154514957430a7a3569506b445738496d774b664b6969334a6d567145746155653365414349376a615a39446d7674493674665454506a346b39765a7075466f444a7930646d430a31687770584d7769514a356a6b5536714a7942375045646b7a39532b6a554534454e6b4356476e4c5032624b376541336465576e354e52544a767170684272450a4f4d4a6a644b645a41674d42414145436767454146572b684b30586f4b485259536e456f513375364b4b2f566a6c6f377a6f507050416437657a3936583553730a776c34506a48626752435a61515a306d722f7a4c4d48434662684a723261556168384864467536464132636c772f676374574b354c354b306b42744352794b370a697378394b616e552f6632755279683658537266506874546f6f4142566e775335364d5769676174787a4c6f707544416e716c4b6f4f46656c463648736831320a6736652b67383332644e62367879656875613578572f6c646e516f39436a674a5763446b496e7a32357a557854335a56626b44624d4a7868794a685a313631530a2b73494265745836544e37735645357336507258704853332f714734673466366d6769484c7133334834537656555a41653955706244774758415936494575650a737a53324c7a6e52776e6379496d4d3735354663484930774d526e346c7142484f786162315a765467514b4267514470575565306e61617364456d564b5a38740a6337773045355732523866444e5a374347766b6f4e46782f34304b72674f6b45716f55675a583578646d332b2b624b75757a5047334d2f56366e79447a7135680a596d35643247696d38653041716531305859447273514350382f37797a7a68376930716a3739796e2f5a414a4b6673626d316a68533879314634705570677a7a0a5844764b7962424c43347770614957506a7a6943707a533332514b42675144673678514c4731414563544f4c6652496d534f597355346f426d724b416f3863300a506b566b454a78453437663654737535756f65436e324a57636d3447584a7434596737527335612b6733576879574d2f33434e4c5866704242517043633573570a4a50704a504832384c6443394645524a506977616955466545634e67345a3630575a556a6975416e6b6a7234355466324a4a4f6e4e316f64672b70506d454c6b0a7341526b3459303767514b42674155764a706973702f644d336857695278634c617a4c382f47614155622f5567534a7531766f397235426e7a434e6a53636f410a7639526f624e613465746b6655776a757638653751434c5167744f7130395432437432713453685556352b634a7470652b5735444548416953356535597466620a3046793042344c7a3779394537333839684576394578387931712f717748376e6e61787a727162384b7245413058625042384a66564a7942416f4741644e4f470a4b4c4b3649475351536e376667345651455777652f6642566b5a34415a624747703541394b306442453849443765666d5a55485765574b637061394b6a67415a0a4248474d396b34674e72583957486c47312b6e72694152504c4f3852656a496730784f5a6c376f516433586b646b725636373670646d77786d4d763466474d660a70554f495a4f562b766a4f4a6d732b713569744a49705758696c706a504a66303446574c333445436759454178413065724d7145437a79685544396e345043500a784f6d693350753353316758674e74774651752f79784b482b676a384d41662f6e6566596f2b6f7169352b74514c5a5559724e3639755830736738736834386a0a316a58543337496a6137474c354973752b677373615361354e4e3875767a725652724668547073626e356f7949615578356a425961424f57542f39444f73356b0a7159585761392f6e587a78613438776b596d71354f4b453d0a2d2d2d2d2d454e442050524956415445204b45592d2d2d2d2d0a
Image Width                     : 512
Image Height                    : 512
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 512x512
Megapixels                      : 0.262



from HEX en cyberchef
-----BEGIN PRIVATE KEY-----
MIIEvQIBADANBgkqhkiG9w0BAQEFAASCBKcwggSjAgEAAoIBAQDNBGX39hQafORZ
z1G0lJ7izHxlEVhn9d3EbelXQX2gpsjfjSeDWQzDiwZFO5ERE8FzVzl1GhQccogR
FoIH4KdKxqezcjpiF/perHvSBdB7/vXo1DyfBQtuFLwxBmTY+Rb/n9PVtujoKoeJ
wey8d5k4T+fuwU5rK9Qgvs+pSwsT67cwrzKBkq0Fujur7wHsHWqTUavEdDATQIWC
z5iPkDW8ImwKfKii3JmVqEtaUe3eACI7jaZ9DmvtI6tfTTPj4k9vZpuFoDJy0dmC
1hwpXMwiQJ5jkU6qJyB7PEdkz9S+jUE4ENkCVGnLP2bK7eA3deWn5NRTJvqphBrE
OMJjdKdZAgMBAAECggEAFW+hK0XoKHRYSnEoQ3u6KK/Vjlo7zoPpPAd7ez96X5Ss
wl4PjHbgRCZaQZ0mr/zLMHCFbhJr2aUah8HdFu6FA2clw/gctWK5L5K0kBtCRyK7
isx9KanU/f2uRyh6XSrfPhtTooABVnwS56MWigatxzLopuDAnqlKoOFelF6Hsh12
g6e+g832dNb6xyehua5xW/ldnQo9CjgJWcDkInz25zUxT3ZVbkDbMJxhyJhZ161S
+sIBetX6TN7sVE5s6PrXpHS3/qG4g4f6mgiHLq33H4SvVUZAe9UpbDwGXAY6IEue
szS2LznRwncyImM755FcHI0wMRn4lqBHOxab1ZvTgQKBgQDpWUe0naasdEmVKZ8t
c7w0E5W2R8fDNZ7CGvkoNFx/40KrgOkEqoUgZX5xdm3++bKuuzPG3M/V6nyDzq5h
Ym5d2Gim8e0Aqe10XYDrsQCP8/7yzzh7i0qj79yn/ZAJKfsbm1jhS8y1F4pUpgzz
XDvKybBLC4wpaIWPjziCpzS32QKBgQDg6xQLG1AEcTOLfRImSOYsU4oBmrKAo8c0
PkVkEJxE47f6Tsu5uoeCn2JWcm4GXJt4Yg7Rs5a+g3WhyWM/3CNLXfpBBQpCc5sW
JPpJPH28LdC9FERJPiwaiUFeEcNg4Z60WZUjiuAnkjr45Tf2JJOnN1odg+pPmELk
sARk4Y07gQKBgAUvJpisp/dM3hWiRxcLazL8/GaAUb/UgSJu1vo9r5BnzCNjScoA
v9RobNa4etkfUwjuv8e7QCLQgtOq09T2Ct2q4ShUV5+cJtpe+W5DEHAiS5e5Ytfb
0Fy0B4Lz7y9E7389hEv9Ex8y1q/qwH7nnaxzrqb8KrEA0XbPB8JfVJyBAoGAdNOG
KLK6IGSQSn7fg4VQEWwe/fBVkZ4AZbGGp5A9K0dBE8ID7efmZUHWeWKcpa9KjgAZ
BHGM9k4gNrX9WHlG1+nriARPLO8RejIg0xOZl7oQd3XkdkrV676pdmwxmMv4fGMf
pUOIZOV+vjOJms+q5itJIpWXilpjPJf04FWL34ECgYEAxA0erMqECzyhUD9n4PCP
xOmi3Pu3S1gXgNtwFQu/yxKH+gj8MAf/nefYo+oqi5+tQLZUYrN69uX0sg8sh48j
1jXT37Ija7GL5Isu+gssaSa5NN8uvzrVRrFhTpsbn5oyIaUx5jBYaBOWT/9DOs5k
qYXWa9/nXzxa48wkYmq5OKE=
-----END PRIVATE KEY-----

ponemos coment en un archivo hex
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ nano key.hex

convertimos a .pem
xxd -r -p key.hex > private.pem



ahora con nuestra key privada

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ openssl pkey -in private.pem -text -noout
Private-Key: (2048 bit, 2 primes)
modulus:
    00:cd:04:65:f7:f6:14:1a:7c:e4:59:cf:51:b4:94:
    9e:e2:cc:7c:65:11:58:67:f5:dd:c4:6d:e9:57:41:
    7d:a0:a6:c8:df:8d:27:83:59:0c:c3:8b:06:45:3b:
    91:11:13:c1:73:57:39:75:1a:14:1c:72:88:11:16:
    82:07:e0:a7:4a:c6:a7:b3:72:3a:62:17:fa:5e:ac:
    7b:d2:05:d0:7b:fe:f5:e8:d4:3c:9f:05:0b:6e:14:
    bc:31:06:64:d8:f9:16:ff:9f:d3:d5:b6:e8:e8:2a:
    87:89:c1:ec:bc:77:99:38:4f:e7:ee:c1:4e:6b:2b:
    d4:20:be:cf:a9:4b:0b:13:eb:b7:30:af:32:81:92:
    ad:05:ba:3b:ab:ef:01:ec:1d:6a:93:51:ab:c4:74:
    30:13:40:85:82:cf:98:8f:90:35:bc:22:6c:0a:7c:
    a8:a2:dc:99:95:a8:4b:5a:51:ed:de:00:22:3b:8d:
    a6:7d:0e:6b:ed:23:ab:5f:4d:33:e3:e2:4f:6f:66:
    9b:85:a0:32:72:d1:d9:82:d6:1c:29:5c:cc:22:40:
    9e:63:91:4e:aa:27:20:7b:3c:47:64:cf:d4:be:8d:
    41:38:10:d9:02:54:69:cb:3f:66:ca:ed:e0:37:75:
    e5:a7:e4:d4:53:26:fa:a9:84:1a:c4:38:c2:63:74:
    a7:59
publicExponent: 65537 (0x10001)
privateExponent:
    15:6f:a1:2b:45:e8:28:74:58:4a:71:28:43:7b:ba:
    28:af:d5:8e:5a:3b:ce:83:e9:3c:07:7b:7b:3f:7a:
    5f:94:ac:c2:5e:0f:8c:76:e0:44:26:5a:41:9d:26:
    af:fc:cb:30:70:85:6e:12:6b:d9:a5:1a:87:c1:dd:
    16:ee:85:03:67:25:c3:f8:1c:b5:62:b9:2f:92:b4:
    90:1b:42:47:22:bb:8a:cc:7d:29:a9:d4:fd:fd:ae:
    47:28:7a:5d:2a:df:3e:1b:53:a2:80:01:56:7c:12:
    e7:a3:16:8a:06:ad:c7:32:e8:a6:e0:c0:9e:a9:4a:
    a0:e1:5e:94:5e:87:b2:1d:76:83:a7:be:83:cd:f6:
    74:d6:fa:c7:27:a1:b9:ae:71:5b:f9:5d:9d:0a:3d:
    0a:38:09:59:c0:e4:22:7c:f6:e7:35:31:4f:76:55:
    6e:40:db:30:9c:61:c8:98:59:d7:ad:52:fa:c2:01:
    7a:d5:fa:4c:de:ec:54:4e:6c:e8:fa:d7:a4:74:b7:
    fe:a1:b8:83:87:fa:9a:08:87:2e:ad:f7:1f:84:af:
    55:46:40:7b:d5:29:6c:3c:06:5c:06:3a:20:4b:9e:
    b3:34:b6:2f:39:d1:c2:77:32:22:63:3b:e7:91:5c:
    1c:8d:30:31:19:f8:96:a0:47:3b:16:9b:d5:9b:d3:
    81
prime1:
    00:e9:59:47:b4:9d:a6:ac:74:49:95:29:9f:2d:73:
    bc:34:13:95:b6:47:c7:c3:35:9e:c2:1a:f9:28:34:
    5c:7f:e3:42:ab:80:e9:04:aa:85:20:65:7e:71:76:
    6d:fe:f9:b2:ae:bb:33:c6:dc:cf:d5:ea:7c:83:ce:
    ae:61:62:6e:5d:d8:68:a6:f1:ed:00:a9:ed:74:5d:
    80:eb:b1:00:8f:f3:fe:f2:cf:38:7b:8b:4a:a3:ef:
    dc:a7:fd:90:09:29:fb:1b:9b:58:e1:4b:cc:b5:17:
    8a:54:a6:0c:f3:5c:3b:ca:c9:b0:4b:0b:8c:29:68:
    85:8f:8f:38:82:a7:34:b7:d9
prime2:
    00:e0:eb:14:0b:1b:50:04:71:33:8b:7d:12:26:48:
    e6:2c:53:8a:01:9a:b2:80:a3:c7:34:3e:45:64:10:
    9c:44:e3:b7:fa:4e:cb:b9:ba:87:82:9f:62:56:72:
    6e:06:5c:9b:78:62:0e:d1:b3:96:be:83:75:a1:c9:
    63:3f:dc:23:4b:5d:fa:41:05:0a:42:73:9b:16:24:
    fa:49:3c:7d:bc:2d:d0:bd:14:44:49:3e:2c:1a:89:
    41:5e:11:c3:60:e1:9e:b4:59:95:23:8a:e0:27:92:
    3a:f8:e5:37:f6:24:93:a7:37:5a:1d:83:ea:4f:98:
    42:e4:b0:04:64:e1:8d:3b:81
exponent1:
    05:2f:26:98:ac:a7:f7:4c:de:15:a2:47:17:0b:6b:
    32:fc:fc:66:80:51:bf:d4:81:22:6e:d6:fa:3d:af:
    90:67:cc:23:63:49:ca:00:bf:d4:68:6c:d6:b8:7a:
    d9:1f:53:08:ee:bf:c7:bb:40:22:d0:82:d3:aa:d3:
    d4:f6:0a:dd:aa:e1:28:54:57:9f:9c:26:da:5e:f9:
    6e:43:10:70:22:4b:97:b9:62:d7:db:d0:5c:b4:07:
    82:f3:ef:2f:44:ef:7f:3d:84:4b:fd:13:1f:32:d6:
    af:ea:c0:7e:e7:9d:ac:73:ae:a6:fc:2a:b1:00:d1:
    76:cf:07:c2:5f:54:9c:81
exponent2:
    74:d3:86:28:b2:ba:20:64:90:4a:7e:df:83:85:50:
    11:6c:1e:fd:f0:55:91:9e:00:65:b1:86:a7:90:3d:
    2b:47:41:13:c2:03:ed:e7:e6:65:41:d6:79:62:9c:
    a5:af:4a:8e:00:19:04:71:8c:f6:4e:20:36:b5:fd:
    58:79:46:d7:e9:eb:88:04:4f:2c:ef:11:7a:32:20:
    d3:13:99:97:ba:10:77:75:e4:76:4a:d5:eb:be:a9:
    76:6c:31:98:cb:f8:7c:63:1f:a5:43:88:64:e5:7e:
    be:33:89:9a:cf:aa:e6:2b:49:22:95:97:8a:5a:63:
    3c:97:f4:e0:55:8b:df:81
coefficient:
    00:c4:0d:1e:ac:ca:84:0b:3c:a1:50:3f:67:e0:f0:
    8f:c4:e9:a2:dc:fb:b7:4b:58:17:80:db:70:15:0b:
    bf:cb:12:87:fa:08:fc:30:07:ff:9d:e7:d8:a3:ea:
    2a:8b:9f:ad:40:b6:54:62:b3:7a:f6:e5:f4:b2:0f:
    2c:87:8f:23:d6:35:d3:df:b2:23:6b:b1:8b:e4:8b:
    2e:fa:0b:2c:69:26:b9:34:df:2e:bf:3a:d5:46:b1:
    61:4e:9b:1b:9f:9a:32:21:a5:31:e6:30:58:68:13:
    96:4f:ff:43:3a:ce:64:a9:85:d6:6b:df:e7:5f:3c:
    5a:e3:cc:24:62:6a:b9:38:a1
    
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ openssl pkeyutl -decrypt -inkey private.pem -in flag.enc -out mensaje.txt


abrimos el archivo

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cat mensaje.txt
academy{rs4_k3y_1n_1mg_21d0a083}

```

```
academy{rs4_k3y_1n_1mg_3e14722a}
```
## Notas adicionales

## Referencias