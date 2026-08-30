## Descripción
What was I last working on? I remember writing a note to help me remember...

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/67/challenge.zip)

Hints

1.- The `cat` command will let you read a file, but that won't help you here!

2.- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).

3.- When committing a file with git, a message can (and should) be included.
## Solución
```
XlayersCeboso-academy@webshell:~$ wget https://artifacts.picoctf.net/c_titan/67/challenge.zip
--2026-08-29 16:22:42--  https://artifacts.picoctf.net/c_titan/67/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.40, 3.160.5.18, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17743 (17K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                              100%[========================================================================================================================================>]  17.33K  --.-KB/s    in 0.004s  

2026-08-29 16:22:43 (4.47 MB/s) - 'challenge.zip' saved [17743/17743]

XlayersCeboso-academy@webshell:~$ ls
Addadshashanammu        HOLA.txt           challenge.zip  convertme.py.1  file       fixme1.py  koala                level2.flag.txt.enc  level3.py   salida.txt     static.ltdis.strings.txt
Addadshashanammu.zip    README.txt         code.py        convertme.py.2  file.1     fixme2.py  l                    level2.py            ltdis.sh    serpentine.py  static.ltdis.x86_64.txt
Addadshashanammu.zip.1  big-zip-files      codebook.txt   enc_flag        files      flag       level1.flag.txt.enc  level3.flag.txt.enc  ltdis.sh.1  static         strings
HOLA                    big-zip-files.zip  convertme.py   enc_flag.1      files.zip  hola       level1.py            level3.hash.bin      runme.py    static.1       warm
XlayersCeboso-academy@webshell:~$ unzip challenge.zip 
Archive:  challenge.zip
   creating: drop-in/
  inflating: drop-in/message.txt     
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/master  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/43/
 extracting: drop-in/.git/objects/43/246218ab4fc7b30e9a9dff073e012316851469  
   creating: drop-in/.git/objects/25/
 extracting: drop-in/.git/objects/25/16effb8d70e33bdd0023629b164a77225e1ec2  
   creating: drop-in/.git/objects/b9/
 extracting: drop-in/.git/objects/b9/2bdd8ec87a21ba45e77bd9bed3e4893faafd0f  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/master  
XlayersCeboso-academy@webshell:~$ cat drop-in/message.txt 
This is what I was working on, but I'd need to look at my commit history to know why...XlayersCeboso-academy@webshell:~$ cd drop-in/.git
XlayersCeboso-academy@webshell:~/drop-in/.git$ git log
XlayersCeboso-academy@webshell:~/drop-in/.git$ 


commit b92bdd8ec87a21ba45e77bd9bed3e4893faafd0f (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:29 2024 +0000

    picoCTF{t1m3m@ch1n3_5cde9075}
```
## Notas Adicionales
## Referencias
- https://webshell.cylabacademy.org/
- https://primer.picoctf.org/#_git_version_control