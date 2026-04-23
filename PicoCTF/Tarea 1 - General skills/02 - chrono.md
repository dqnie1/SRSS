
# Descripción

How to automate tasks to run at intervals on linux servers?Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 62448
Username: picoplayer 
Password: emrdK96SGH
```

# Solución

```
┌──(daniel㉿kali)-[~]
└─$ ssh picoplayer@saturn.picoctf.net -p 53744                
The authenticity of host '[saturn.picoctf.net]:53744 ([13.59.203.175]:53744)' can't be established.
ED25519 key fingerprint is: SHA256:dMTscRrUiURy7uMu5eGWwEKdd2FzqLzx6LfWhssWnNQ
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:1: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:53744' (ED25519) to the list of known hosts.
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.8.0-1047-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

picoplayer@challenge:~$ find / -name "*flag*" -type f 2>/dev/null | head -20
/proc/sys/kernel/acpi_video_flags
/proc/sys/net/ipv4/fib_notify_on_flag_change
/proc/sys/net/ipv6/fib_notify_on_flag_change
/proc/kpageflags
/sys/devices/pnp0/00:04/00:04:0/00:04:0.0/tty/ttyS0/flags
/sys/devices/platform/serial8250/serial8250:0/serial8250:0.3/tty/ttyS3/flags
/sys/devices/platform/serial8250/serial8250:0/serial8250:0.1/tty/ttyS1/flags
/sys/devices/platform/serial8250/serial8250:0/serial8250:0.2/tty/ttyS2/flags
/sys/devices/virtual/net/eth0/flags
/sys/devices/virtual/net/lo/flags
/sys/module/scsi_mod/parameters/default_dev_flags
picoplayer@challenge:~$ crontab -l
no crontab for picoplayer
picoplayer@challenge:~$ ls -la /etc/cron.hourly/
total 4
drwxr-xr-x 2 root root  26 Aug  4  2023 .
drwxr-xr-x 1 root root  66 Apr 19 01:23 ..
-rw-r--r-- 1 root root 102 Feb 13  2020 .placeholder
picoplayer@challenge:~$ ls -la /etc/cron.daily/
total 12
drwxr-xr-x 1 root root   26 Aug  4  2023 .
drwxr-xr-x 1 root root   66 Apr 19 01:23 ..
-rw-r--r-- 1 root root  102 Feb 13  2020 .placeholder
-rwxr-xr-x 1 root root 1478 Apr  9  2020 apt-compat
-rwxr-xr-x 1 root root 1187 Sep  5  2019 dpkg
picoplayer@challenge:~$ ls -la /etc/cron.weekly/
total 4
drwxr-xr-x 2 root root  26 Aug  4  2023 .
drwxr-xr-x 1 root root  66 Apr 19 01:23 ..
-rw-r--r-- 1 root root 102 Feb 13  2020 .placeholder
picoplayer@challenge:~$ ls -la /etc/cron.d/
total 8
drwxr-xr-x 1 root root  26 Aug  4  2023 .
drwxr-xr-x 1 root root  66 Apr 19 01:23 ..
-rw-r--r-- 1 root root 102 Feb 13  2020 .placeholder
-rw-r--r-- 1 root root 201 Feb 14  2020 e2scrub_all
picoplayer@challenge:~$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_0bb95b71}

```


# Notas adicionales

# Referencias
