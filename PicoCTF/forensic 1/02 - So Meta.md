# Descripción
Find the flag in this picture.

# Solución
```
┌──(daniel㉿kali)-[~/So_meta]
└─$ strings pico_img.png | grep pico
picoCTF{s0_m3ta_19ebefe2}
```

# Notas adicionales
Los **metadatos** son, de forma sencilla, **"datos sobre otros datos"**.

Imagina que un archivo (una foto, un PDF o un video) es un sobre cerrado. El contenido del sobre es la información principal, pero lo que está escrito por fuera (quién lo envía, la fecha, el sello postal, el peso) son los metadatos. No son el mensaje en sí, pero describen todo el contexto de ese mensaje.

También se puede hacer con una herramienta para ver metadatos.
# Referencias
Gemini