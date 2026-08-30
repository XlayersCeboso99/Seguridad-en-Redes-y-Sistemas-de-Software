## Descripción
I accidentally wrote the flag down. Good thing I deleted it!

You download the challenge files here:.

- [challenge.zip](https://artifacts.picoctf.net/c_titan/138/challenge.zip)

Hints

1.- Version control can help you recover files if you change or lose them!

2.- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control)

3.- You can 'checkout' commits to see the files inside them
## Solución
```
XlayersCeboso-academy@webshell:~$ wget https://artifacts.picoctf.net/c_titan/138/challenge.zip
--2026-08-30 03:40:07--  https://artifacts.picoctf.net/c_titan/138/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.95, 3.160.5.40, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19199 (19K) [application/octet-stream]
Saving to: 'challenge.zip.7'

challenge.zip.7                                            100%[========================================================================================================================================>]  18.75K  --.-KB/s    in 0.002s  

2026-08-30 03:40:07 (11.9 MB/s) - 'challenge.zip.7' saved [19199/19199]

XlayersCeboso-academy@webshell:~$ unzip challenge.zip 
Archive:  challenge.zip
replace drop-in/message.txt? [y]es, [n]o, [A]ll, [N]one, [r]ename: A
  inflating: drop-in/message.txt     
  inflating: drop-in/.git/description  
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
  inflating: drop-in/.git/info/exclude  
 extracting: drop-in/.git/refs/heads/master  
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
 extracting: drop-in/.git/objects/43/246218ab4fc7b30e9a9dff073e012316851469  
 extracting: drop-in/.git/objects/25/16effb8d70e33bdd0023629b164a77225e1ec2  
 extracting: drop-in/.git/objects/b9/2bdd8ec87a21ba45e77bd9bed3e4893faafd0f  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
  inflating: drop-in/.git/logs/HEAD  
  inflating: drop-in/.git/logs/refs/heads/master  
XlayersCeboso-academy@webshell:~$ la -la
total 10188
drwxr-xr-x   8 XlayersCeboso-academy XlayersCeboso-academy    4096 Aug 30 03:40 .
drwxr-xr-x   3 root                  root                       63 Aug 19 16:20 ..
-rw-r--r--   1 XlayersCeboso-academy XlayersCeboso-academy     220 Aug 19 16:20 .bash_logout
-rw-r--r--   1 XlayersCeboso-academy XlayersCeboso-academy    3771 Aug 19 16:20 .bashrc
-rw-------   1 XlayersCeboso-academy XlayersCeboso-academy      20 Aug 30 03:37 .lesshst
drwxrwxr-x   3 XlayersCeboso-academy XlayersCeboso-academy      19 Aug 26 16:39 .local
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy       0 Aug 24 17:00 .ltdis.x86_64.txt
-rw-r--r--   1 XlayersCeboso-academy XlayersCeboso-academy     807 Aug 19 16:20 .profile
drwx------   2 XlayersCeboso-academy XlayersCeboso-academy      48 Aug 28 23:24 .ssh
drwxr-xr-x   3 XlayersCeboso-academy XlayersCeboso-academy      28 Dec 12  2025 Addadshashanammu
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy    5166 Dec 12  2025 Addadshashanammu.zip
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy    5166 Dec 12  2025 Addadshashanammu.zip.1
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy  287385 Aug 20 03:25 HOLA
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy  287393 Aug 20 03:26 HOLA.txt
-rw-r--r--   1 root                  root                     4510 Aug 30 03:39 README.txt
drwxrwxr-x 121 XlayersCeboso-academy XlayersCeboso-academy   28672 May  3  2020 big-zip-files
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy 3182988 Jun 30 01:12 big-zip-files.zip
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy   17743 Mar 11  2024 challenge.zip
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy  293587 Mar 12  2024 challenge.zip.1
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy  293587 Mar 12  2024 challenge.zip.2
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy   24467 Mar 11  2024 challenge.zip.3
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy   24467 Mar 11  2024 challenge.zip.4
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy   19199 Mar 12  2024 challenge.zip.5
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy   19199 Mar 12  2024 challenge.zip.6
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy   19199 Mar 12  2024 challenge.zip.7
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy    1278 Jun 30 01:08 code.py
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy      27 Jun 30 01:08 codebook.txt
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy    1189 Jun 30 01:12 convertme.py
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy    1189 Jun 30 01:12 convertme.py.1
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy    1189 Jun 30 01:12 convertme.py.2
drwxr-xr-x   4 XlayersCeboso-academy XlayersCeboso-academy      73 Aug 30 03:40 drop-in
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy     349 Jun 30 01:14 enc_flag
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy     349 Jun 30 01:14 enc_flag.1
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy   14546 Oct 31  2025 file
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy   14546 Oct 31  2025 file.1
drwxrwxr-x   5 XlayersCeboso-academy XlayersCeboso-academy     124 May 13  2022 files
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy 3995553 Jun 30 01:09 files.zip
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy     835 Aug 26 16:40 fixme1.py
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy    1031 Aug 26 16:47 fixme2.py
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy      34 Dec 12  2025 flag
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy  287867 Aug 20 03:29 hola
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy  286811 Aug 20 03:40 koala
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy       1 Aug 26 16:46 l
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy      30 Jun 30 01:11 level1.flag.txt.enc
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy     876 Jun 30 01:11 level1.py
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy      31 Jun 30 01:09 level2.flag.txt.enc
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy     914 Jun 30 01:09 level2.py
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy      31 Jun 30 01:12 level3.flag.txt.enc
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy      16 Jun 30 01:12 level3.hash.bin
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy    1337 Jun 30 01:12 level3.py
-rwxrwxr-x   1 XlayersCeboso-academy XlayersCeboso-academy     785 Dec 12  2025 ltdis.sh
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy     785 Dec 12  2025 ltdis.sh.1
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy     270 Jun 30 01:10 runme.py
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy  287858 Aug 20 03:27 salida.txt
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy    2569 Aug 26 17:18 serpentine.py
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy   16776 Dec 12  2025 static
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy   16776 Dec 12  2025 static.1
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy    1699 Aug 25 01:43 static.ltdis.strings.txt
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy    6363 Aug 25 01:43 static.ltdis.x86_64.txt
-rw-rw-r--   1 XlayersCeboso-academy XlayersCeboso-academy  784424 Nov 14  2025 strings
-rwxrwxr-x   1 XlayersCeboso-academy XlayersCeboso-academy   19312 Dec 12  2025 warm
XlayersCeboso-academy@webshell:~$ git init
XlayersCeboso-academy@webshell:~/drop-in$ cd ~
XlayersCeboso-academy@webshell:~$ mkdir commitment138
XlayersCeboso-academy@webshell:~$ cd commitment138
XlayersCeboso-academy@webshell:~/commitment138$ unzip ~/challenge.zip.7
Archive:  /home/XlayersCeboso-academy/challenge.zip.7
   creating: drop-in/
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
   creating: drop-in/.git/objects/0e/
 extracting: drop-in/.git/objects/0e/0fefcdc9c9722914a7a9ecab1e88784f005eeb  
   creating: drop-in/.git/objects/5b/
 extracting: drop-in/.git/objects/5b/222fb49097fe9874695e8cc7cd9a6c80886017  
   creating: drop-in/.git/objects/b5/
 extracting: drop-in/.git/objects/b5/62f0b425907789d11d2fe2793e67592dc6be93  
   creating: drop-in/.git/objects/d5/
 extracting: drop-in/.git/objects/d5/52d1ecd2d83fa2e65b6724d1ff73b45a7d59b7  
   creating: drop-in/.git/objects/0c/
 extracting: drop-in/.git/objects/0c/1ab266b7a3a1cd099bb509f82b7a2d03aecd03  
   creating: drop-in/.git/objects/42/
 extracting: drop-in/.git/objects/42/942c9c605b30100f5d859ef6e172027447c0db  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/master  
 extracting: drop-in/message.txt     
XlayersCeboso-academy@webshell:~/commitment138$ cd drop-in
XlayersCeboso-academy@webshell:~/commitment138/drop-in$ ls -la
total 4
drwxr-xr-x 3 XlayersCeboso-academy XlayersCeboso-academy  37 Mar 12  2024 .
drwxrwxr-x 3 XlayersCeboso-academy XlayersCeboso-academy  21 Aug 30 03:45 ..
drwxr-xr-x 8 XlayersCeboso-academy XlayersCeboso-academy 166 Mar 12  2024 .git
-rw-r--r-- 1 XlayersCeboso-academy XlayersCeboso-academy  11 Mar 12  2024 message.txt
XlayersCeboso-academy@webshell:~/commitment138/drop-in$ git --no-pager log --oneline
42942c9 (HEAD -> master) remove sensitive info
b562f0b create flag
XlayersCeboso-academy@webshell:~/commitment138/drop-in$ git show b562f0b
XlayersCeboso-academy@webshell:~/commitment138/drop-in$ 
```
## Notas Adicionales
## Referencias
- https://webshell.cylabacademy.org/
- https://primer.picoctf.org/#_git_version_control
- https://chatgpt.com/