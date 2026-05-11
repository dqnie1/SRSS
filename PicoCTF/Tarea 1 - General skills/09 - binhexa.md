# Descripción 
How well can you perfom basic binary operations?

Start searching for the flag here `nc titan.picoctf.net 58578`
# Solución

```
┌──(daniel㉿kali)-[~]
└─$ nc titan.picoctf.net 58578

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 01011010
Binary Number 2: 11001001


Question 1/6:
Operation 1: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11011011                  
Correct!

Question 2/6:
Operation 2: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 01001000
Correct!

Question 3/6:
Operation 3: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 100011010101010
Correct!

Question 4/6:
Operation 4: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 100100011
Correct!

Question 5/6:
Operation 5: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 10110100
Correct!

Question 6/6:
Operation 6: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 01100100
Correct!

Enter the results of the last operation in hexadecimal: 64

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_675602ae}
```
# Notas adicionales

Solo resolver las operaciones
# Referencias


