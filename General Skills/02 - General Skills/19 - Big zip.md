## Descripción
Unzip this archive and find the flag.

## Solución
```
wget https://artifacts.picoctf.net/c/504/big-zip-files.zip

unzip big-zip-files.zip

XlayersCeboso-academy@webshell:~$ grep -r "pico" big-zip-files/
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}

- picoCTF{gr3p_15_m4g1c_ef8790dc}
```
## Notas Adicionales
- grep -r "pico" big-zip-files/ 

- Con grep llamamos la herramienta de busqueda con -r hacemos el proceso recursivo y colocamos la palabra a buscar seguido del directorio con / al final
## Referencias
- https://webshell.cylabacademy.org/
- https://shibushivansh.medium.com/picoctf-big-zip-runme-py-music-serpentine-plumbing-first-find-based-f1f1fddfe092