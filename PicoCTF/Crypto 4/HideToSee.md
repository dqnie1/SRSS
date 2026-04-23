# Descripción
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/236/atbash.jpg).

# Solución

```
┌──(daniel㉿kali)-[/]
└─$ sudo steghide extract -sf atbash.jpg.1                  
Anotar salvoconducto: 
anot� los datos extra�dos e/"encrypted.txt".
                                                                                                                                                                       
┌──(daniel㉿kali)-[/]
└─$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_zx751vx6}
                                                                                                                                                                       
┌──(daniel㉿kali)-[/]
└─$ echo "krxlXGU{zgyzhs_xizxp_zx751vx6}" | tr 'A-Za-z' 'ZYXWVUTSRQPONMLKJIHGFEDCBAzyxwvutsrqponmlkjihgfedcba'
picoCTF{atbash_crack_ac751ec6}

```

# Referencia
