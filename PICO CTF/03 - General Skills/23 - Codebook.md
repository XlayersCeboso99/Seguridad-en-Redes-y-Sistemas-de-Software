## Descripción
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/3/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/3/codebook.txt)
## Solución
```
XlayersCeboso-academy@webshell:~$ wget https://artifacts.picoctf.net/c/3/code.py
--2026-08-26 16:20:28--  https://artifacts.picoctf.net/c/3/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.64, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                                                    100%[========================================================================================================================================>]   1.25K  --.-KB/s    in 0s      

2026-08-26 16:20:28 (61.9 MB/s) - 'code.py' saved [1278/1278]

XlayersCeboso-academy@webshell:~$ wget https://artifacts.picoctf.net/c/3/codebook.txt
--2026-08-26 16:20:44--  https://artifacts.picoctf.net/c/3/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.95, 3.160.5.64, 3.160.5.40, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt                                               100%[========================================================================================================================================>]      27  --.-KB/s    in 0s      

2026-08-26 16:20:44 (1.41 MB/s) - 'codebook.txt' saved [27/27]

XlayersCeboso-academy@webshell:~$ python3 code.py
picoCTF{c0d3b00k_455157_197a982c}
```
## Notas Adicionales
- Algunos scripts al ejecutarse es posible que requieran la existencia de otros archivos para poder trabajar
- nano - es un editor en modo texto de linux y se usa Ctrl x para salir 

## Referencias
- https://webshell.cylabacademy.org/