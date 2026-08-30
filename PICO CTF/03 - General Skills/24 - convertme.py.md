## Descripción
Run the Python script and convert the given number from decimal to binary to get the flag.

[Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)

## Solución
```
XlayersCeboso-academy@webshell:~$ wget https://artifacts.picoctf.net/c/24/convertme.py
--2026-08-26 16:32:30--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.40, 3.160.5.64, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py.2'

convertme.py.2                                             100%[========================================================================================================================================>]   1.16K  --.-KB/s    in 0s      

2026-08-26 16:32:30 (396 MB/s) - 'convertme.py.2' saved [1189/1189]

XlayersCeboso-academy@webshell:~$ python3 convertme.py 
If 61 is in decimal base, what is it in binary base?
Answer: 111101
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}

XlayersCeboso-academy@webshell:~$ python3 
Python 3.10.12 (main, Mar  3 2026, 11:56:32) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> bin(61)
'0b111101'
>>> 
```
## Notas Adicionales
## Referencias
- https://webshell.cylabacademy.org/