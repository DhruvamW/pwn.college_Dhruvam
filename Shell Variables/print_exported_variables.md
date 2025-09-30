# PRINTING EXPORTING VARIABLES
In this challenge I have to access exported variables.

## My solve
**Flag:** `pwn.college{E2_OdvLYWHfqKekO88o95W5DJa3.QX4UTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to use the env command to view all the exported variables. One of the variables was FLAG with the flag as its value.
```bash
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=b471235bb9e49215b5d19279122d1be593c32940ee15ee5b42e34ceb418895fa
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{E2_OdvLYWHfqKekO88o95W5DJa3.QX4UTN0wiN4EzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

## What I learned
Through this challenge I learnt that: 
- env command: it'll print out every exported variable set in your shell.

## References
No references used.

