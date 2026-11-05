
## Descripción

What can you do with this file? I forgot the key to my safe but this [file](https://challenge-files.cylabacademy.net/library/5c5f8143dd09275a5ecdd390027ea5488159881d757099706515c4cbf15992f1/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?

1.- Download and try to decompile the file.

## Solución
```
┌──(kali㉿kali)-[~]
└─$ mkdir safeopener                              
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ cd safeopener 
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/safeopener]
└─$ wget https://challenge-files.cylabacademy.net/library/5c5f8143dd09275a5ecdd390027ea5488159881d757099706515c4cbf15992f1/SafeOpener.class
--2026-11-04 11:19:31--  https://challenge-files.cylabacademy.net/library/5c5f8143dd09275a5ecdd390027ea5488159881d757099706515c4cbf15992f1/SafeOpener.class
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.22, 13.226.187.37, 13.226.187.40, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.22|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2036 (2.0K) [application/octet-stream]
Saving to: ‘SafeOpener.class’

SafeOpener.class                                           100%[========================================================================================================================================>]   1.99K  --.-KB/s    in 0s      

2026-11-04 11:19:33 (70.1 MB/s) - ‘SafeOpener.class’ saved [2036/2036]

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/safeopener]
└─$ ls      
SafeOpener.class
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/safeopener]
└─$ strings -n10 SafeOpener.class                          
LineNumberTable
LocalVariableTable
LSafeOpener;
([Ljava/lang/String;)V
[Ljava/lang/String;
Ljava/io/BufferedReader;
InnerClasses
Ljava/util/Base64$Encoder;
encodedkey
Ljava/lang/String;
StackMapTable
Exceptions
(Ljava/lang/String;)Z
SourceFile
SafeOpener.java
java/io/BufferedReader
java/io/InputStreamReader
Enter password for the safe: 
java/lang/StringBuilder
You have  
 attempt(s) left
,academy{SAf3_0p3n3rr_y0u_solv3d_it_7f70e636}
Sesame open
Password is incorrect
SafeOpener
java/lang/Object
java/util/Base64$Encoder
java/lang/String
java/io/IOException
java/lang/System
Ljava/io/InputStream;
(Ljava/io/InputStream;)V
(Ljava/io/Reader;)V
java/util/Base64
getEncoder
()Ljava/util/Base64$Encoder;
Ljava/io/PrintStream;
java/io/PrintStream
(Ljava/lang/String;)V
()Ljava/lang/String;
encodeToString
([B)Ljava/lang/String;
-(Ljava/lang/String;)Ljava/lang/StringBuilder;
(I)Ljava/lang/StringBuilder;
(Ljava/lang/Object;)Z
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/safeopener]
└─$ strings -n10 SafeOpener.class | grep aca        
,academy{SAf3_0p3n3rr_y0u_solv3d_it_7f70e636}


academy{SAf3_0p3n3rr_y0u_solv3d_it_7f70e636}

```

## Notas Adicionales

## Referencias
