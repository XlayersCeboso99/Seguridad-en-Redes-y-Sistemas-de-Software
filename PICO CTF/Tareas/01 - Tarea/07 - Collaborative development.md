## Descripción
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?

You can download the challenge files here:.

- [challenge.zip](https://artifacts.picoctf.net/c_titan/71/challenge.zip)

1.- `git branch -a` will let you see available branches

2.- How can file 'diffs' be brought to the main branch? Don't forget to `git config`!

3.- Merge conflicts can be tricky! Try a text editor like nano, emacs, or vim.
## Solución
```
Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

PS C:\Users\sebas> wget https://artifacts.picoctf.net/c_titan/71/challenge.zip

Advertencia de seguridad: riesgo de ejecución de script
Invoke-WebRequest analiza el contenido de la página web. El código de script de la página web se puede ejecutar cuando
se analiza la página.
      ACCIÓN RECOMENDADA:
      Usa el modificador -UseBasicParsing para evitar la ejecución de código de script.

      ¿Quieres continuar?

[S] Sí  [O] Sí a todo  [N] No  [T] No a todo  [U] Suspender  [?] Ayuda (el valor predeterminado es "N"): S


StatusCode        : 200
StatusDescription : OK
Content           : {80, 75, 3, 4...}
RawContent        : HTTP/1.1 200 OK
                    Connection: keep-alive
                    x-amz-server-side-encryption: AES256
                    x-amz-version-id: ZYOKXZQOWW1hHFvPytyy0TqwvxYhHDnz
                    X-Cache: Miss from cloudfront
                    X-Amz-Cf-Pop: QRO53-P2
                    X-Amz-Cf-Id: 8...
Headers           : {[Connection, keep-alive], [x-amz-server-side-encryption, AES256], [x-amz-version-id,
                    ZYOKXZQOWW1hHFvPytyy0TqwvxYhHDnz], [X-Cache, Miss from cloudfront]...}
RawContentLength  : 24467



PS C:\Users\sebas> Invoke-WebRequest -Uri "https://artifacts.picoctf.net/c_titan/71/challenge.zip" -OutFile "challenge.zip"
PS C:\Users\sebas> dir challenge.zip


    Directorio: C:\Users\sebas


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----     29/08/2026  08:54 p. m.          24467 challenge.zip


PS C:\Users\sebas> Expand-Archive -Path .\challenge.zip -DestinationPath .\challenge
PS C:\Users\sebas> cd .\challenge
PS C:\Users\sebas\challenge> dir -Force


    Directorio: C:\Users\sebas\challenge


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----     29/08/2026  08:55 p. m.                drop-in


PS C:\Users\sebas\challenge> cd .\drop-in
PS C:\Users\sebas\challenge\drop-in> git status
On branch main
nothing to commit, working tree clean
PS C:\Users\sebas\challenge\drop-in> git branch -a
  feature/part-1
  feature/part-2
  feature/part-3
* main
PS C:\Users\sebas\challenge\drop-in> git show feature/part-1:flag.py
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')
PS C:\Users\sebas\challenge\drop-in> git show feature/part-2:flag.py
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')
PS C:\Users\sebas\challenge\drop-in> git show feature/part-3:flag.py
print("Printing the flag...")

print("w0rk_4c24302f}")
PS C:\Users\sebas\challenge\drop-in>


- picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_4c24302f}
```
## Notas Adicionales
## Referencias
- https://webshell.cylabacademy.org/
- https://chatgpt.com/