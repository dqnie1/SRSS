# Descripción 
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.

Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/18/challenge.zip)
# Solución

```

┌──(daniel㉿kali)-[~]
└─$ ssh -p 52525 ctf-player@atlas.picoctf.net
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Lower! Try again.
Enter your guess: 750
Lower! Try again.
Enter your guess: 900
Lower! Try again.
Enter your guess: 1000
Lower! Try again.
Enter your guess: 300
Higher! Try again.
Enter your guess: 
Please enter a valid number.
Enter your guess: 200
Higher! Try again.
Enter your guess: 250
Higher! Try again.
Enter your guess: 300
Higher! Try again.
Enter your guess: 350
Lower! Try again.
Enter your guess: 325
Congratulations! You guessed the correct number: 325
Here's your flag: picoCTF{g00d_gu355_2e90d29b}
Connection to atlas.picoctf.net closed.
                                                                             

```
# Notas adicionales

Nada más es adivinar
# Referencias


