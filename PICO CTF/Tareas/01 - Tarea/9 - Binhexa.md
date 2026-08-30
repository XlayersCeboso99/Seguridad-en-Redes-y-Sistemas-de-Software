## Descripción
How well can you perfom basic binary operations?

Start searching for the flag here `nc titan.picoctf.net 56943`
## Solución
```
XlayersCeboso-academy@webshell:~$ ssh -p 58944 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:58944 ([18.217.83.136]:58944)' can't be established.
ED25519 key fingerprint is SHA256:M8hXanE8l/Yzfs8iuxNsuFL4vCzCKEIlM/3hpO13tfQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:58944' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
XlayersCeboso-academy@webshell:~$ nc titan.picoctf.net 64919

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 11011011
Binary Number 2: 00101101


Question 1/6:
Operation 1: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 01001001
Incorrect. Try again
Enter the binary result: 00101111
Incorrect. Try again
Enter the binary result: 

Incorrect input. Provide the right input
Enter the binary result: 00101101
Incorrect. Try again
Enter the binary result: 00010110
Correct!

Question 2/6:
Operation 2: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10011001111111
Correct!

Question 3/6:
Operation 3: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 100001000
Correct!

Question 4/6:
Operation 4: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 110110110
Correct!

Question 5/6:
Operation 5: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00001001
Correct!

Question 6/6:
Operation 6: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11111111
Correct!

Enter the results of the last operation in hexadecimal: FF

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d6f8047e}
How well can you perfom basic binary operations?

Start searching for the flag here `nc titan.picoctf.net 56943`
```
## Notas Adicionales
## Referencias
- https://webshell.cylabacademy.org/