# Descripción
Download this disk image and find the flag. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/137/disk.flag.img.gz)
# Solución
```
 ┌──(daniel㉿kali)-[~]
└─$ fls -o 0000360448 disk.flag.img 1995 -r
r/r 2363:       .ash_history
d/d 3981:       my_folder
+ r/r * 2082(realloc):  flag.txt
+ r/r 2371:     flag.uni.txt
                                                                             
┌──(daniel㉿kali)-[~]
└─$ icat -o 0000360448 disk.flag.img 2371
picoCTF{by73_5urf3r_adac6cb4}

```
# Notas adicionales
-FLS -O
-ICAT -O

# Referencias