# Descripción
Can you look at the data in this binary? The bash script might help![static](https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/static), [ltdis.sh](https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/ltdis.sh)

# Solución


```
danielqueee-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/ltdis.sh
--2026-02-11 14:23:50--  https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/ltdis.sh
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.18, 3.160.5.95, 3.160.5.40, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh'

ltdis.sh                                        100%[=====================================================================================================>]     785  --.-KB/s    in 0s      

2026-02-11 14:23:51 (231 MB/s) - 'ltdis.sh' saved [785/785]

danielqueee-picoctf@webshell:~$ ./ltdis.sh static
-bash: ./ltdis.sh: Permission denied
danielqueee-picoctf@webshell:~$ chmod +x ltdis.sh
danielqueee-picoctf@webshell:~$ 
danielqueee-picoctf@webshell:~$ ./ltdis.sh 
Attempting disassembly of  ...
objdump: 'a.out': No such file
objdump: section '.text' mentioned in a -j option, but not found in any input file
Disassembly failed!
Usage: ltdis.sh <program-file>
Bye!
danielqueee-picoctf@webshell:~$ ./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
danielqueee-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_20335e41}
```
# Notas adicionales
usando strings y grep

# Referencias
