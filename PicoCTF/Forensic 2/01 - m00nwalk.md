# Descripción
Decode this [message](https://challenge-files.picoctf.net/c_fickle_tempest/d372c5aa057b687f120292b30c70af827c64bd3661490e3e2f41551ff95394f0/message.wav) from the moon.

# Solución


```
┌──(daniel㉿kali)-[~]
└─$ cd Descargas                                    
                                                                             
┌──(daniel㉿kali)-[~/Descargas]
└─$ ls
'garden(1).jpg'   garden.jpg
                                                                             
┌──(daniel㉿kali)-[~/Descargas]
└─$ strings garden.jpg | grep pico                  
Here is a flag: picoCTF{more_than_m33ts_the_3y398ee229a}
```

# Notas adicionales
También se puede hacer con una herramienta dentro de kali
# Referencias