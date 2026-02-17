# Descripción
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)

# Solución
```
2026-02-17 01:57:53 (144 MB/s) - 'runme.py' saved [270/270]

danielqueee-picoctf@webshell:~$ ls
README.txt         enc_flag   runme.py                  strings
big-zip-files      files      static.ltdis.strings.txt
big-zip-files.zip  files.zip  static.ltdis.x86_64.txt
danielqueee-picoctf@webshell:~$ python runme.py 
picoCTF{run_s4n1ty_run}
```

# Notas adicionales
Correr el script de picoCTF, primero descargarlo. wget para el webshell
python nombre_archivo


# Referencias