# Descripción
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/07bf5ee832c595a6de406476b6c07f164d2951fbcfcf9cf3739c25dea26e5f0b/capture.pcap). Recover the flag.

# Solución


```

wireshark capture.pcap &  

udp.stream eq 32
udp.stream eq 60

udp.dstport == 22

>>> chr(112)
'p'
>>> chr(105)
'i'
>>> chr(99)
'c'
>>> chr(111)
'o'

sudo apt install python3-scapy 

from scapy.all import *

packets = rdpcap('capture.pcap')

flag=''

for p in packets:
    if UDP in p and p[UDP].dport == 22:
        if p[UDP].sport > 5000:
            flag+=chr(p[UDP].sport - 5000)

print(flag)
```


# Notas adicionales

# Referencias
[picoGym (picoCTF) Exercise: shark on wire 2](https://www.youtube.com/watch?v=FU6NBjB6lJQ)