# Descripción
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)

# Solución
```
danielqueee-picoctf@webshell:~$ python fixme2.py 
  File "/home/danielqueee-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
danielqueee-picoctf@webshell:~$ nano fixme2.py 
danielqueee-picoctf@webshell:~$ python fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```
# Notas adicionales
Error de sintaxis de usar "="

# Referencias