## Descripción
Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/563d66bbed3925c75ed71efa974bfafab26460ae99938d699a8881cd173fca60/strings) without running it?
## Solución
Primero hice wget
```
wget https://challenge-files.picoctf.net/c_fickle_tempest/563d66bbed3925c75ed71efa974bfafab26460ae99938d699a8881cd173fca60/strings
```

- Luego hice file strings
-  Cat strings
- Strings strings 
- Finalmente: Strings strings | grep pico 

```
XlayersCeboso-academy@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_dB2CEA76}
```
## Notas Adicionales
- Strings muestra las caenas (caracteres imprimibles) en un archivo binario (no texto)

## Referencias
- https://webshell.cylabacademy.org/