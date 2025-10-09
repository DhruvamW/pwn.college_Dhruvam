# USING SUDO
In this challenge I have to use sudo priveleges to read the flag.

## My solve
**Flag:** `pwn.college{ILCDGiphKo7Xt2l3-vQB9H5bTGf.QX4UDN1wiN4EzNzEzW}`

It was mentioned in the problem statement that I have sudo access and I have to read the flag. First I tried reading the flag normally but then I used sudo to read the flag.
```bash
hacker@users~using-sudo:~$ cat /flag
cat: /flag: Permission denied
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{ILCDGiphKo7Xt2l3-vQB9H5bTGf.QX4UDN1wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-   root passwords are a pain to maintain, they (or their hashes!) can leak, and they don't lend themselves well to larger environments
- Unlike su, which defaults to launching a shell as a specified user, sudo defaults to running a command as root
-  sudo checks policies to determine whether the user is authorized to run commands as root

## References
No references used.

