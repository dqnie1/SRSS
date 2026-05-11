# Descripción 
I accidentally wrote the flag down. Good thing I deleted it!

You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/77/challenge.zip)

# Solución

```
┌──(daniel㉿kali)-[~]
└─$ cd drop-in/
                                                                             
┌──(daniel㉿kali)-[~/drop-in]
└─$ ls -la
total 16
drwxr-xr-x  3 daniel daniel 4096 mar  9  2024 .
drwx------ 23 daniel daniel 4096 may 11 14:34 ..
drwxr-xr-x  8 daniel daniel 4096 mar  9  2024 .git
-rw-r--r--  1 daniel daniel   11 mar  9  2024 message.txt
                                                                             
┌──(daniel㉿kali)-[~/drop-in]
└─$ git log
commit e1237df82d2e69f62dd53279abc1c8aeb66f6d64 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:14 2024 +0000

    remove sensitive info

commit 3d5ec8a26ee7b092a1760fea18f384c35e435139
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:14 2024 +0000

    create flag
                                                                             
┌──(daniel㉿kali)-[~/drop-in]
└─$ git checkout e1237df82d2e69f62dd53279abc1c8aeb66f6d64
Nota: cambiando a 'e1237df82d2e69f62dd53279abc1c8aeb66f6d64'.

Te encuentras en estado 'detached HEAD'. Puedes revisar por aquí, hacer
cambios experimentales y hacer commits, y puedes descartar cualquier
commit que hayas hecho en este estado sin impactar a tu rama realizando
otro checkout.

Si quieres crear una nueva rama para mantener los commits que has creado,
puedes hacerlo (ahora o después) usando -c con el comando checkout. Ejemplo:

  git switch -c <nombre-de-nueva-rama>

O deshacer la operación con:

  git switch -

Desactiva este aviso poniendo la variable de config advice.detachedHead en false

HEAD está ahora en e1237df remove sensitive info
                                                                             
┌──(daniel㉿kali)-[~/drop-in]
└─$ cat message.txt
TOP SECRET
                                                                             
┌──(daniel㉿kali)-[~/drop-in]
└─$ 
                                                                             
┌──(daniel㉿kali)-[~/drop-in]
└─$ git checkout 3d5ec8a26ee7b092a1760fea18f384c35e435139
La posición previa de HEAD era e1237df remove sensitive info
HEAD está ahora en 3d5ec8a create flag
                                                                             
┌──(daniel㉿kali)-[~/drop-in]
└─$ cat message.txt
picoCTF{s@n1t1z3_30e86d36}

```
# Notas adicionales

Usar los comandos de git para volver a contenido ya eliminado

# Referencias


