# LEARNING COMPLEX USAGE
In this challenge I have to run a command with an argument as given in the documentation.

## My solve
**Flag:** `pwn.college{cGJ4BVsrEjEvz6xxN4ERZt3C0VQ.QX1ITO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to read the documentation to understand what to do. The documentation of this problem stated that I have to ivoke the '/challenge/challenge' command with '--printfile' argument which takes a path to a file as its argument.
```bash
hacker@man~learning-complex-usage:~$ ls /
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{cGJ4BVsrEjEvz6xxN4ERZt3C0VQ.QX1ITO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that usage of some commands can get quite complex. There are commands that take arguments to their arguments like the 'find -name' command.

## References 
No references used.

