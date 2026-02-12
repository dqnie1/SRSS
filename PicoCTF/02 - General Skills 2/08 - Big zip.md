# Descripción
Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/503/big-zip-files.zip)

# Solución
```
  inflating: big-zip-files/mktyhgmedcj.txt  
danielqueee-picoctf@webshell:~$ grep -r pico
README.txt:Welcome to the picoCTF webshell!
README.txt:picoCTF challenges.
README.txt:other@picoctf.org and we will consider adding it.
README.txt:  Extensive brute-forcing is not necessary to solve picoCTF challenges.
README.txt:- If you change your username through the picoCTF website, you will
.python_history:nc fickle-tempest.picoctf.net at port 50697
.bash_history:nc wily-courier.picoctf.net 50828
grep: strings: binary file matches
static.ltdis.strings.txt:   3020 picoCTF{d15a5m_t34s3r_20335e41}
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
```

# Notas adicionales
Se descarga, unzip, y con un grep -r busca en todos los archivos la bandera

# Referencias
