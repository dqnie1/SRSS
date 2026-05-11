# Descripción 
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/70/challenge.zip)
# Solución

```

┌──(daniel㉿kali)-[~/drop-in]
└─$ cat flag.py 
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')                                                                             
┌──(daniel㉿kali)-[~/drop-in]
└─$ git checkout feature/part-2
Cambiado a rama 'feature/part-2'
                                                                             
┌──(daniel㉿kali)-[~/drop-in]
└─$ cat flag.py
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')                                                                             
┌──(daniel㉿kali)-[~/drop-in]
└─$ git checkout feature/part-3
Cambiado a rama 'feature/part-3'
                                                                             
┌──(daniel㉿kali)-[~/drop-in]
└─$ cat flag.py                
print("Printing the flag...")

print("w0rk_7ffa0077}")


```
# Notas adicionales

cambiamos de rama para ir armando la flag
# Referencias


