## Descripción
Fix the syntax error in the Python script to print the flag.

[Download Python script](https://artifacts.picoctf.net/c/4/fixme2.py)
## Solución
```
XlayersCeboso-academy@webshell:~$ wget https://artifacts.picoctf.net/c/4/fixme2.py
--2026-08-26 16:44:37--  https://artifacts.picoctf.net/c/4/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.95, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                                                  100%[========================================================================================================================================>]   1.00K  --.-KB/s    in 0s      

2026-08-26 16:44:37 (256 MB/s) - 'fixme2.py' saved [1029/1029]

XlayersCeboso-academy@webshell:~$ python2 fixme2.py
-bash: python2: command not found
XlayersCeboso-academy@webshell:~$ ls
Addadshashanammu        HOLA        big-zip-files      codebook.txt    convertme.py.2  file    files.zip  flag   ltdis.sh    salida.txt  static.ltdis.strings.txt  warm
Addadshashanammu.zip    HOLA.txt    big-zip-files.zip  convertme.py    enc_flag        file.1  fixme1.py  hola   ltdis.sh.1  static      static.ltdis.x86_64.txt
Addadshashanammu.zip.1  README.txt  code.py            convertme.py.1  enc_flag.1      files   fixme2.py  koala  runme.py    static.1    strings
XlayersCeboso-academy@webshell:~$ python3 fixme2.py
  File "/home/XlayersCeboso-academy/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
XlayersCeboso-academy@webshell:~$ nano - l fixme2.py
Reading data from keyboard; type ^D or ^D^D to finish.
XlayersCeboso-academy@webshell:~$ python3 fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}

```
## Notas Adicionales
## Referencias
- https://webshell.cylabacademy.org/