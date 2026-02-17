# Descripción
Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/36/serpentine.py)

# Solución
```
danielqueee-picoctf@webshell:~$ nano serpentine.py 
danielqueee-picoctf@webshell:~$ python serpentine.py 

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_aa2340b2}

Oops! I must have misplaced the print_flag function! Check my source code!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) ^CTraceback (most recent call last):
  File "/home/danielqueee-picoctf/serpentine.py", line 81, in <module>
    main()
  File "/home/danielqueee-picoctf/serpentine.py", line 63, in main
    choice = input('What would you like to do? (a/b/c) ')
KeyboardInterrupt
```

# Notas adicionales

# Referencias