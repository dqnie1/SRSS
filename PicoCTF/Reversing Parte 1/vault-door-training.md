# Descripción

# Solución 
```
┌──(daniel㉿kali)-[~]
└─$ wget https://challenge-files.picoctf.net/c_fickle_tempest/379ca32f89b74c70403ef5b6515ae2f1d2405e66735347b70bc2ef8063084688/VaultDoorTraining.java  
--2026-04-29 08:49:10--  https://challenge-files.picoctf.net/c_fickle_tempest/379ca32f89b74c70403ef5b6515ae2f1d2405e66735347b70bc2ef8063084688/VaultDoorTraining.java
Resolviendo challenge-files.picoctf.net (challenge-files.picoctf.net)... 18.238.132.49, 18.238.132.115, 18.238.132.26, ...
Conectando con challenge-files.picoctf.net (challenge-files.picoctf.net)[18.238.132.49]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 943 [application/octet-stream]
Grabando a: «VaultDoorTraining.java»

VaultDoorTraining.j 100%[================>]     943  --.-KB/s    en 0s      

2026-04-29 08:49:11 (38.4 MB/s) - «VaultDoorTraining.java» guardado [943/943]

                                                                             
┌──(daniel㉿kali)-[~]
└─$ cat VaultDoorTraining.java 
import java.util.*;

class VaultDoorTraining {
    public static void main(String args[]) {
        VaultDoorTraining vaultDoor = new VaultDoorTraining();
        Scanner scanner = new Scanner(System.in); 
        System.out.print("Enter vault password: ");
        String userInput = scanner.next();
        String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
        if (vaultDoor.checkPassword(input)) {
            System.out.println("Access granted.");
        } else {
            System.out.println("Access denied!");
        }
   }

    // The password is below. Is it safe to put the password in the source code?
    // What if somebody stole our source code? Then they would know what our
    // password is. Hmm... I will think of some ways to improve the security
    // on the other doors.
    //
    // -Minion #9567
    public boolean checkPassword(String password) {
        return password.equals("w4rm1ng_Up_w1tH_jAv4_000wYdiGTvt");
    }
}
      
```
# Referencias

