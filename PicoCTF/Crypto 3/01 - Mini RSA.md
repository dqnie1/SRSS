# Descripción
What happens if you have a small exponent? There is a twist though, we padded the plaintext so that (M ** e) is just barely larger than N. Let's decrypt this:[values](https://challenge-files.picoctf.net/c_wily_courier/26f56c2d4fc3ff842ad67a8a7536ba110d4b40f7b36eea831285f892795710de/values)

# Solución

```
sudo apt install python3-gmpy2
```

Código que se uso de python:
```
import gmpy2

n = ...
e = ...
c = ... 

print("Calculando la raíz cúbica de c...")

m, es_exacta = gmpy2.iroot(c, 3)

if es_exacta:
    print("\n¡Raíz cúbica perfecta encontrada!")
    print(f"Mensaje (entero): {m}")
    flag = bytes.fromhex(hex(m)[2:]).decode()
    print(f"FLAG: {flag}")
else:
    print("\nNo se encontró una raíz cúbica perfecta.")
    print("Este ataque (small e) no funcionó.")
```

Solo cambiamos los valores de las variables por las que vienen en el archivo values.

# Referencias
Discord
 