## Descripción
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.

Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!.

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/5/challenge.zip)

`ssh -p 58944 ctf-player@atlas.picoctf.net`

Using the password `1ad5be0d`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!

Instance

Expires in 29:54

Hints

1.- Have you ever played hot or cold? Binary search is a bit like that.

2.- You have a very limited number of guesses. Try larger jumps between numbers!

3.- The program will randomly choose a new number each time you connect. You can always try again, but you should start your binary search over from the beginning - try around 500. Can you think of why?
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
Enter your guess: 250
Higher! Try again.
Enter your guess: 300
Higher! Try again.
Enter your guess: 350
Higher! Try again.
Enter your guess: 400
Higher! Try again.
Enter your guess: 450
Higher! Try again.
Enter your guess: 475
Higher! Try again.
Enter your guess: 480 
Higher! Try again.
Enter your guess: 490
Higher! Try again.
Enter your guess: 495
Higher! Try again.
Enter your guess: 500
Higher! Try again.
Sorry, you've exceeded the maximum number of guesses.
Connection to atlas.picoctf.net closed.
XlayersCeboso-academy@webshell:~$ ssh -p 58944 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Lower! Try again.
Enter your guess: 250
Lower! Try again.
Enter your guess: 100
Lower! Try again.
Enter your guess: 50
Higher! Try again.
Enter your guess: 60
Higher! Try again.
Enter your guess: 70
Lower! Try again.
Enter your guess: 65
Higher! Try again.
Enter your guess: 68
Lower! Try again.
Enter your guess: 67
Congratulations! You guessed the correct number: 67
Here's your flag: picoCTF{g00d_gu355_3af33d18}
Connection to atlas.picoctf.net closed.
XlayersCeboso-academy@webshell:~$ 
```
## Notas Adicionales
## Referencias
- https://webshell.cylabacademy.org/
-  https://chatgpt.com/