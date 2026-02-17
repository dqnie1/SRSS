# Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

# Solución
```
danielqueee-picoctf@webshell:~$ nano level3.py 
danielqueee-picoctf@webshell:~$ ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]
-bash: [f09e,: command not found
danielqueee-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: f09e
That password is incorrect
danielqueee-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 4dcf
That password is incorrect
danielqueee-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
```
# Notas adicionales
Descargar 3 archivos
echo
cat para el hash
nannoononononononnono

# Referencias