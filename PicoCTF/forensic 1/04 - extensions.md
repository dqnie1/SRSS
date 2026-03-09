# Descripción
This is a really weird text file. Can you find the flag? Get the flag from [TXT](https://challenge-files.picoctf.net/c_fickle_tempest/31fe772e6a4c71e867af0b2a93818e06d8f8ebf8af2a9615495d00356ff576da/flag.txt).

# Solución

```
┌──(daniel㉿kali)-[~/extensions]
└─$ mv flag.txt flag.png
                                                                             
┌──(daniel㉿kali)-[~/extensions]
└─$ ls                              
flag.png
                                                                             
┌──(daniel㉿kali)-[~/extensions]
└─$ open flag.png
```
# Notas adicionales

Los **Magic Bytes** (también conocidos como _file signatures_ o números mágicos) son los primeros bytes de un archivo que sirven como una "huella digital" para que el sistema operativo o un software identifiquen de qué tipo de archivo se trata, independientemente de la extensión que tenga.

Si le cambias el nombre a una foto de `vacaciones.png` a `vacaciones.txt`, tu computadora seguirá sabiendo que es una imagen porque leerá los **Magic Bytes** al principio del código hexadecimal del archivo.

---

### Los Magic Bytes de un PNG

Un archivo PNG siempre comienza con una secuencia específica de **8 bytes**. Aquí los tienes en sus diferentes formatos:

|Formato|Valor de los Magic Bytes|
|---|---|
|**Hexadecimal**|`89 50 4E 47 0D 0A 1A 0A`|
|**Representación ASCII**|`. P N G . . . .`|
# Referencias
Gemini